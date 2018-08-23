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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 81f35f659342d6258d60f40b12bd0a3ac2dc20b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588476"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
1 つまたは複数の受信者のエントリの名前解決を実行します。
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpPropTagArray_
  
> [in]プロバイダーによって返された[ADRLIST](adrlist.md)構造体に含まれるプロパティを記述するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 プロバイダーの既定のプロパティのセットを要求するには、 _lpPropTagArray_パラメーターに NULL を渡します。 
    
 _ulFlags_
  
> [in]返される文字列内のテキストの種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
EMS_AB_ADDRESS_LOOKUP
  
> 正確なプロキシ アドレスの一致のみが検索されます。部分的な一致は無視されます。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。
    
MAPI_CACHE_ONLY
  
> 名前解決を実行するのには、オフライン アドレス帳のみが使用されます。 たとえば、exchange キャッシュ モードでグローバル アドレス一覧 (GAL) を開き、クライアントとサーバー間のトラフィックを作成することがなく、キャッシュからそのアドレス帳のエントリにアクセスするのにクライアント アプリケーションを有効にするのにこのフラグを使用することができます。 このフラグは、Exchange のアドレス帳プロバイダーでのみサポートします。 
    
MAPI_UNICODE 
  
> Unicode 形式では、返される文字列のプロパティです。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _lpAdrList_
  
> [で [チェック アウト]入力、解決するのには受信者のリストを格納する**ADRLIST**構造体へのポインター。 出力では、解決された名前を格納する**ADRLIST**構造体へのポインター。 
    
 _lpFlagList_
  
> [で [チェック アウト]フラグの配列へのポインター、 _lpAdrList_のパラメーターに[ADRENTRY](adrentry.md)構造体に対応する各フラグを提供する、受信者の名前解決操作のステータス。 _LpAdrList_内のエントリと同じ順序では、 _lpFlagList_パラメーター内のフラグです。 次のフラグを設定することができます。
    
MAPI_AMBIGUOUS 
  
> 対応する受信者が解決されていませんが、エントリの一意の識別子です。 他のコンテナーは、この受信者を解決するのにはいけません。 
    
MAPI_RESOLVED 
  
> エントリの一意の識別子に対応する受信者を解決されています。 他のコンテナーは、この受信者を解決するのにはいけません。 
    
MAPI_UNRESOLVED 
  
> 対応するエントリが解決されていません。 他のコンテナーは、この受信者を解決するようにしてください。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 名前解決の処理が正常に完了しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダーは、このメソッドを使用して一括名前解決をサポートしていません。
    
## <a name="remarks"></a>注釈

**ResolveNames**メソッドは、このアドレス帳コンテナー内の受信者に、 _lpAdrList_パラメーター内のエントリの配列からの未解決の受信者に一致しようとします。 未解決の受信者には、通常、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティのみと可能性のあるいくつかの他のプロパティがあります。 未解決の受信者にプロパティがない、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) と MAPI_UNRESOLVED に、 _lpFlagList_パラメーターに対応する、フラグを設定します。 逆に、解決済みの受信者は常に少なくとも**PR_ENTRYID**プロパティと**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))、 **PR_DISPLAY_NAME**、 **PR_ADDRTYPE** ([などの他のいくつかのプロパティPidTagAddressType](pidtagaddresstype-canonical-property.md))。
  
名前解決は、クライアントが、 [IAddrBook::ResolveName](iaddrbook-resolvename.md)メソッドを呼び出すと通常起動します。 Outlook MAPI は、 **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) のプロパティで指定されたアドレス帳検索パスに含まれるそれぞれのアドレス帳コンテナーの**ResolveNames**メソッドを呼び出すことによって応答します。 _LpAdrList_パラメーター内のエントリには、受信者検索パスの前のエントリが表示されるための MAPI が既に呼び出されて**ResolveNames**コンテナーにいるので、既に解決にはが含まれます。 
  
各コンテナーは、そのエントリのいずれかの表示名と、受信者の表示名を照合することによって、未解決のエントリを解決するしようとします。 一意の一致が見つかると、 **ResolveNames** **PR_ENTRYID**プロパティと送信の**ADRLIST**構造体の対応するエントリを_lpPropTagArray_パラメーターに含まれるその他のプロパティを追加します。 **ResolveNames** MAPI_RESOLVED に_lpFlagList_パラメーターにエントリを設定します。 **PR_ENTRYID**プロパティに格納されているエントリの識別子は、短期的または長期的にできます。 
  
結局のところ、検索で使用するコンテナーのパスが試行されると名前解決プロセス、MAPI ダイアログが開き、可能であれば、残りの競合を解決するのにユーザーに確認します。 
  
クライアントでは、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドの呼び出しで返された**ADRLIST**構造体を使用することも。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**ResolveNames**メソッドを使用して名前解決をサポートする必要はありません。 代わりに、またはさらは、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) のプロパティの制限をサポートできます。 名前解決のための**PR_ANR**の制限に依存している場合は、MAPI_E_NO_SUPPORT を返すことができます。 詳細については、[名前解決の実装](implementing-name-resolution.md)を参照してください。
  
コンテナーの受信者のいずれかの受信者に一致しない場合は、MAPI_UNRESOLVED、 _lpFlagList_パラメーターで、受信者のフラグのエントリを設定します。 
  
受信者には、複数の受信者が一致すると、そのフラグを MAPI_AMBIGUOUS に設定しの**ADRENTRY**の構造を変更しないでください。 
  
MAPI には、メッセージの受信者のリストに含まれる受信者の特定のプロパティが必要です。 名前解決プロセスの一環としての**ADRENTRY**構造体に含まれてまたは[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)と[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)メソッドの呼び出しを要求したときに MAPI を待機できます。 これらの余分な呼び出しを削除および解決済みのすべての受信者の**ADRENTRY**構造体の次のプロパティを含めることによってパフォーマンスを向上できます。 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME**([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
_LpPropTagArray_パラメーターのプロパティの一部が表示されません-通常コンテナーのエントリがサポートされていないためプロパティとそれらに含まれない**ADRLIST**構造内の受信者の**ADRENTRY**のメンバー。PT_ERROR に使用できない各プロパティのプロパティの種類を設定します。 
  
解決済みの受信者の**ADRENTRY**構造体からプロパティを削除されません。 
  
必要があります交換ではなく、 **ADRENTRY**構造体を変更する場合、は、最初に関数を呼び出して、 [MAPIFreeBuffer](mapifreebuffer.md) 、元の**ADRENTRY**構造体を解放し、交換用の[と**ADRENTRY**の構造体を割り当てるMAPIAllocateBuffer](mapiallocatebuffer.md)。
  
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

