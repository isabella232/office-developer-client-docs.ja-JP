---
title: imapisupportaddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407320"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[共通のアドレス] ダイアログボックスを表示します。 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>パラメーター

 _l出 uiparam_
  
> [入力]ダイアログボックスの親ウィンドウのハンドルへのポインター。 入力時には、ウィンドウハンドルを常に渡す必要があります。 出力時に、DIALOG_SDI フラグが_lpadrparms_パラメーターで示される[ADRPARM](adrparm.md)構造で設定されている場合は、モードレスダイアログボックスのウィンドウハンドルが返されます。 
    
 _lpadrparms_
  
> [入力][アドレス] ダイアログボックスの表示と動作を制御する**ADRPARM**構造体へのポインター。 
    
 _lppadrlist_
  
> [入力]アドレス一覧へのポインターへのポインター。 入力時に、このリストは、メッセージ内の受信者の現在のリストまたは NULL (リストが存在しない場合) のいずれかです。 出力では、 _lppadrlist_は、更新されたメッセージ受信者のリストを指します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> [アドレス] ダイアログボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: address**メソッドは、アドレス帳プロバイダーサポートオブジェクトに実装されています。 アドレス帳プロバイダーの呼び出し**アドレス**。メッセージの受信者の一覧を作成または更新します。 
  
各受信者は[adrentry](adrentry.md)構造で記述されており、 _lppadrlist_パラメーターで示される[adrentry](adrlist.md)構造体に含まれています。 **adrentry**構造には、受信者のプロパティ値の配列、1つは受信者の種類、または**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティが含まれます。 この**adrlist**構造は、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)の呼び出しで_lpMods_パラメーターとして使用するために、クライアントに渡すことができます。
  
**adrlist**構造内の各受信者は解決できます。これは、そのプロパティ値のいずれかが**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティであるか、または未解決であることを示します。これは、 **PR_ENTRYID**プロパティがれ. 
  
**PR_ENTRYID**に加えて、解決された受信者には次のプロパティが含まれています。
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
未解決の受信者には、通常、 **PR_DISPLAY_NAME**と**PR_RECIPIENT_TYPE**のみが含まれます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

発信者が渡す**adrlist**構造は、MAPI が返す構造体のサイズと異なる場合があります。 **adrlist**構造体のメモリを割り当てるときは、各[spropvalue](spropvalue.md)構造体のメモリを個別に割り当てます。 
  
[abproviderinit](abproviderinit.md)関数に渡される MAPI メモリ割り当て関数へのポインターを使用して、メモリを割り当てます。 adrlist の[MAPIAllocateBuffer](mapiallocatebuffer.md)関数と**** 、adrlist の**adrlist**構造の各プロパティの値構造**** に、メモリを割り当てます。 
  
**address**がより大きな**adrlist**構造を返す必要がある場合、または_lppadrlist_に NULL が渡された場合、 **address**は元の構造を解放し、新しい構造を割り当てます。 また、**アドレス**は**adrlist**構造に追加のプロパティ値構造を割り当て、必要に応じて古いものを解放します。 **adrlist**構造体のメモリの管理方法の詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。
  
 _lpadrparms_パラメーターの**ADRPARM**構造で DIALOG_SDI フラグが設定されている場合、**アドレス**はすぐに戻ります。 
  
## <a name="see-also"></a>関連項目



[ABProviderInit](abproviderinit.md)
  
[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagAddressType 標準プロパティ](pidtagaddresstype-canonical-property.md)
  
[PidTagDisplayName 標準プロパティ](pidtagdisplayname-canonical-property.md)
  
[PidTagDisplayType 標準プロパティ](pidtagdisplaytype-canonical-property.md)
  
[PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md)
  
[PidTagRecipientType 標準プロパティ](pidtagrecipienttype-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[adrlist および srowset 構造のためのメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)

