---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279571"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数の受信者エントリの名前解決を実行します。
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>パラメーター

 _lpPropTagArray_
  
> 順番プロバイダーによって返される[adrlist](adrlist.md)構造に含まれるプロパティを説明するプロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 プロバイダーの既定のプロパティセットを要求するには、 _lpPropTagArray_パラメーターに NULL を渡します。 
    
 _ulFlags_
  
> 順番返される文字列内のテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
EMS_AB_ADDRESS_LOOKUP
  
> 完全に一致するプロキシアドレスのみが検索されます。部分一致は無視されます。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するために使用されるのは、オフラインアドレス帳のみです。 たとえば、このフラグを使用して、クライアントアプリケーションが exchange キャッシュモードでグローバルアドレス一覧 (GAL) を開き、クライアントとサーバーの間のトラフィックを作成せずに、キャッシュからそのアドレス帳のエントリにアクセスできるようにすることができます。 このフラグは、Exchange アドレス帳プロバイダーによってのみサポートされています。 
    
MAPI_UNICODE 
  
> 返される文字列プロパティは、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _lpadrlist_
  
> [入力]入力時に、解決される受信者のリストを含む**adrlist**構造体へのポインター。 出力時に、解決された名前を含む**adrlist**構造体へのポインター。 
    
 _lpflaglist_
  
> [入力]フラグの配列へのポインター。 _lpadrlist_パラメーターの[adrentry](adrentry.md)構造に対応する各フラグは、受信者の名前解決操作の状態を提供します。 _lpflaglist_パラメーターのフラグは、 _lpadrlist_のエントリと同じ順序になっています。 次のフラグを設定できます。
    
MAPI_AMBIGUOUS 
  
> 対応する受信者は解決されましたが、一意のエントリ識別子は解決されていません。 他のコンテナーは、この受信者の解決を試みてはなりません。 
    
MAPI_RESOLVED 
  
> 対応する受信者が一意のエントリ識別子に解決されました。 他のコンテナーは、この受信者の解決を試みてはなりません。 
    
MAPI_UNRESOLVED 
  
> 対応するエントリは解決されていません。 他のコンテナーは、この受信者の解決を試行する必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 名前解決プロセスが正常に完了しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダーは、このメソッドを使用したバルク名解決をサポートしていません。
    
## <a name="remarks"></a>解説

**ResolveNames**メソッドは、解決されない受信者を、 _lpadrlist_パラメーター内のエントリの配列から、このアドレス帳コンテナー内の受信者に一致させようとします。 未解決の受信者には、通常、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティだけがあり、他にもいくつかのプロパティがあります。 未解決の受信者には、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティがありません。 _lpflaglist_パラメーター内の対応するフラグは MAPI_UNRESOLVED に設定されています。 反対に、解決された受信者には、少なくとも**PR_ENTRYID**プロパティと、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))、 **PR_DISPLAY_NAME**、 **PR_ADDRTYPE**などのその他のプロパティがあります ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
通常、クライアントが[IAddrBook:: ResolveName](iaddrbook-resolvename.md)メソッドを呼び出すときに、名前解決が開始されます。 Outlook MAPI は、 **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティによって指定されたアドレス帳の検索パスに含まれる各アドレス帳コンテナーの**ResolveNames**メソッドを呼び出すことによって応答します。 _lpadrlist_パラメーターのエントリには、検索パスの前にエントリが表示されているため、MAPI が既に**ResolveNames**を呼び出しているコンテナーにあるため、既に解決されている受信者が含まれています。 
  
各コンテナーは、受信者の表示名とそのエントリの表示名を一致させることによって、未解決のエントリの解決を試みます。 一意の一致が見つかった場合、 **ResolveNames**は、 **PR_ENTRYID**プロパティと、 _lpPropTagArray_パラメーターに含まれるその他のプロパティを、出力する**adrlist**構造体の対応するエントリに追加します。 **ResolveNames**は、 _lpflaglist_パラメーターのエントリを MAPI_RESOLVED に設定します。 **PR_ENTRYID**プロパティに格納されているエントリ識別子は、短期的または長期間の場合があります。 
  
検索パス内のすべてのコンテナーが名前解決プロセスを試行した後、MAPI によっては、可能であれば、残りの競合を解決するためにユーザーに支援を求めるダイアログボックスが表示されます。 
  
クライアントは、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドへの呼び出しで、返された**adrlist**構造を使用することもできます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**ResolveNames**メソッドを使用して名前解決をサポートする必要はありません。 代わりに、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティ制限を使用してサポートすることもできます。 名前解決の**PR_ANR**制限に頼る場合は、MAPI_E_NO_SUPPORT を取得することができます。 For more information, see [Implementing Name Resolution](implementing-name-resolution.md).
  
受信者がコンテナーのどの受信者とも一致しない場合は、 _lpflaglist_パラメーターの受信者のフラグエントリを MAPI_UNRESOLVED に設定します。 
  
受信者が複数の受信者と一致する場合は、そのフラグを MAPI_AMBIGUOUS に設定し、 **adrentry**構造を変更しないようにします。 
  
MAPI では、メッセージの宛先リストに含まれる受信者に特定のプロパティが必要です。 名前解決プロセスの一部として、これらを**adrentry**構造に含めるか、MAPI が[IAddrBook::P reparerecips](iaddrbook-preparerecips.md)メソッドと[imapisupport:: ExpandRecips](imapisupport-expandrecips.md)メソッドへの呼び出しを要求するようにすることができます。 解決されたすべての受信者の**adrentry**構造に次のプロパティを含めることで、これらの余分な呼び出しを排除し、パフォーマンスを向上させることができます。 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
_lpPropTagArray_パラメーターの一部のプロパティが使用できない場合 (通常は container エントリがプロパティをサポートしておらず、かつ、 **adrentry**構造の受信者の**adrentry**メンバーに含まれていないためです)。使用できない各プロパティのプロパティの種類を PT_ERROR に設定します。 
  
解決された受信者の**adrentry**構造からはプロパティを削除しないでください。 
  
**adrentry**構造を変更するのではなく、最初に元の**adrentry**構造を解放する必要がある場合は、まず、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、次のように**** [置き換えられた adrentry 構造をMAPIAllocateBuffer](mapiallocatebuffer.md)。
  
## <a name="see-also"></a>関連項目



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[PidTagAnr 標準プロパティ](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

