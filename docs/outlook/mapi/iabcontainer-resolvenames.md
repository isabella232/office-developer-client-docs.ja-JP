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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405815"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上の受信者エントリの名前解決を実行します。
  
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
  
> [in]プロバイダーによって返される[ADRLIST](adrlist.md)構造体に含まれるプロパティを記述するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 プロバイダーの既定のプロパティ セットを要求するには  _、lpPropTagArray_ パラメーターに NULL を渡します。 
    
 _ulFlags_
  
> [in]返される文字列内のテキストの種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
EMS_AB_ADDRESS_LOOKUP
  
> プロキシ アドレスの完全一致だけが見つかる。部分一致は無視されます。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するには、オフライン アドレス帳だけが使用されます。 たとえば、このフラグを使用すると、クライアント アプリケーションがキャッシュされた Exchange モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成せずにキャッシュからそのアドレス帳のエントリにアクセスできます。 このフラグは、アドレス帳プロバイダー Exchangeサポートされます。 
    
MAPI_UNICODE 
  
> 返される文字列プロパティは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _lpAdrList_
  
> [in, out]入力時に、解決する受信者の一覧を含む **ADRLIST** 構造体へのポインター。 出力時に、解決された名前を含む **ADRLIST** 構造体へのポインター。 
    
 _lpFlagList_
  
> [in, out]_lpAdrList_ パラメーター内の [ADRENTRY](adrentry.md)構造体に対応する各フラグの配列へのポインターで、受信者の名前解決操作の状態を提供します。 _lpFlagList パラメーターの_ フラグは _、lpAdrList_ のエントリと同じ順序です。 次のフラグを設定できます。
    
MAPI_AMBIGUOUS 
  
> 対応する受信者は解決されましたが、一意のエントリ識別子には解決されません。 他のコンテナーは、この受信者の解決を試みる必要があります。 
    
MAPI_RESOLVED 
  
> 対応する受信者が一意のエントリ識別子に解決されました。 他のコンテナーは、この受信者の解決を試みる必要があります。 
    
MAPI_UNRESOLVED 
  
> 対応するエントリは解決されません。 他のコンテナーは、この受信者の解決を試みる必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 名前解決プロセスが成功しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダーは、このメソッドを使用して一括名前解決をサポートしていない。
    
## <a name="remarks"></a>注釈

**ResolveNames** メソッドは _、lpAdrList_ パラメーター内のエントリの配列から、このアドレス帳コンテナー内の受信者に未解決の受信者を一致します。 未解決の受信者は、通常、PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティのみを持ち、その他のいくつかのプロパティを持つ場合があります。 未解決の受信者には **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティが設定されていないので  _、lpFlagList_ パラメーターの対応するフラグは MAPI_UNRESOLVED に設定されます。 逆に、解決された受信者には、少なくとも **PR_ENTRYID** プロパティと **、PR_EMAIL_ADDRESS** [(PidTagEmailAddress)、PR_DISPLAY_NAME、](pidtagemailaddress-canonical-property.md)および **PR_ADDRTYPE** **(** [PidTagAddressType)](pidtagaddresstype-canonical-property.md)などの他のいくつかのプロパティが常にあります。
  
名前の解決は、通常、クライアントが [IAddrBook::ResolveName メソッドを呼び出した場合に開始](iaddrbook-resolvename.md) されます。 OutlookMAPI は、PR_AB_SEARCH_PATH **(** [PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) プロパティで指定されたアドレス帳検索パスに含まれる各アドレス帳コンテナーの **ResolveNames** メソッドを呼び出して応答します。 _lpAdrList_ パラメーターのエントリには、MAPI が既に **ResolveNames** を呼び出しているコンテナー内にあるため、既に解決済みの受信者が含まれます。これは、エントリが検索パスの前に表示されるからです。 
  
各コンテナーは、受信者の表示名とそのエントリの 1 つの表示名を照合して、未解決のエントリを解決します。 一意の一致が見つかった場合 **、ResolveNames** は _、lpPropTagArray_ パラメーターに含まれる **PR_ENTRYID** プロパティおよび他のプロパティを、送信 **ADRLIST** 構造体の対応するエントリに追加します。 **ResolveNames は**_、lpFlagList_ パラメーター内のエントリを次の値MAPI_RESOLVED。 PR_ENTRYID プロパティに格納 **されている** エントリ識別子は、短期的または長期的に指定できます。 
  
検索パス内のすべてのコンテナーが名前解決プロセスを試みた後、MAPI はダイアログ ボックスを開き、可能であれば、残りの競合を解決するためのヘルプをユーザーに求めるプロンプトを表示します。 
  
クライアントは [、IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドの呼び出しで返される **ADRLIST** 構造体を使用できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**ResolveNames** メソッドで名前解決をサポートする必要はありません。 代わりに、またはさらに、このプロパティをサポートするには、PR_ANR **(** [PidTagAnr](pidtaganr-canonical-property.md)) プロパティの制限を使用します。 名前解決の制限に依存PR_ANR **場合は** 、名前を返MAPI_E_NO_SUPPORT。 For more information, see [Implementing Name Resolution](implementing-name-resolution.md).
  
受信者がコンテナーの受信者と一致しない場合は  _、lpFlagList_ パラメーターの受信者のフラグ エントリを MAPI_UNRESOLVED に設定します。 
  
受信者が複数の受信者と一致する場合は、そのフラグを [MAPI_AMBIGUOUS] に設定し **、ADRENTRY 構造を変更** しない。 
  
MAPI には、メッセージの受信者リストに含まれる受信者の特定のプロパティが必要です。 名前解決プロセスの一部として **ADRENTRY** 構造に含めるか、MAPI が [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) および [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) メソッドへの呼び出しで要求するのを待ちます。 解決済みのすべての受信者の **ADRENTRY** 構造に次のプロパティを含め、これらの余分な呼び出しを排除し、パフォーマンスを向上させることができます。 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
_lpPropTagArray_ パラメーターのプロパティの一部が使用できない場合 (通常、コンテナー エントリはプロパティをサポートしていないので **、ADRLIST** 構造体の受信者の **ADRENTRY** メンバーに含まれていないため)、使用できない各プロパティのプロパティの種類を PT_ERROR に設定します。 
  
解決済み受信者の **ADRENTRY** 構造からプロパティを削除しない。 
  
**ADRENTRY** 構造体を変更するのではなく、置き換える必要がある場合は [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して最初に元の **ADRENTRY** 構造体を解放し、MAPIAllocateBuffer で置換 **ADRENTRY** 構造体を割り当てる必要があります。 [](mapiallocatebuffer.md)
  
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

