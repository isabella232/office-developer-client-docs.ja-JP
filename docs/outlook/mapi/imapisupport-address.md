---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ee1a45deedc733d016d20fbd5cb43dbfa3b6b495
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625491"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[共通アドレス] ダイアログ ボックスを表示します。 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>パラメーター

 _lpulUIParam_
  
> [in, out]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。 入力時には、ウィンドウ ハンドルを常に渡す必要があります。 出力時に _、lpAdrParms_ パラメーターが指す [ADRPARM](adrparm.md)構造で DIALOG_SDI フラグが設定されている場合は、モードレス ダイアログ ボックスのウィンドウ ハンドルが返されます。 
    
 _lpAdrParms_
  
> [in, out]アドレス ダイアログ ボックスの表示と動作を制御する **ADRPARM** 構造体へのポインター。 
    
 _lppAdrList_
  
> [in, out]アドレス一覧へのポインターを指すポインター。 入力時に、このリストはメッセージ内の受信者の現在のリストか、そのようなリストが存在しない場合は NULL のいずれかです。 出力時に  _、lppAdrList は_ メッセージ受信者の更新されたリストをポイントします。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> [アドレス] ダイアログ ボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::Address** メソッドは、アドレス帳プロバイダーのサポート オブジェクトに実装されます。 アドレス帳プロバイダーは、 **アドレスを呼び出** して、メッセージ受信者のリストを作成または更新します。 
  
各受信者は [、lppAdrList](adrentry.md) パラメーターが指す [ADRLIST](adrlist.md) 構造に含まれる  _ADRENTRY 構造で説明_ されています。 **ADRENTRY** 構造体には、受信者プロパティ値の配列が含まれます。そのうちの **1** つは受信者の種類、または PR_RECIPIENT_TYPE ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティです。 この **ADRLIST** 構造体をクライアントに渡して [、IMessage::ModifyRecipients](imessage-modifyrecipients.md)の呼び出しで _lpMods_ パラメーターとして使用できます。
  
**ADRLIST** 構造体の各受信者は、プロパティ値の **1** つが PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティであることを示す解決済みか、**または未解決で、PR_ENTRYID** プロパティが見つからないかどうかを示します。 
  
解決済み受信者 **には、PR_ENTRYID** に加えて、次のプロパティが含まれます。
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
未解決の受信者には、通常、PR_DISPLAY_NAME **と** PR_RECIPIENT_TYPE のみを **含PR_RECIPIENT_TYPE。** 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

呼 **び出し元が渡す ADRLIST** 構造は、MAPI が返す構造とは異なるサイズである可能性があります。 **ADRLIST** 構造体のメモリを割り当てる場合は [、SPropValue](spropvalue.md)構造体ごとに個別にメモリを割り当てる必要があります。 
  
メモリを割り当てるには [、ABProviderInit](abproviderinit.md) 関数に渡される MAPI メモリ割り当て関数へのポインターを使用します。 ADRLIST の [MAPIAllocateBuffer](mapiallocatebuffer.md) 関数を使用してメモリを割り当て **、ADRLIST** の **ADRENTRY** 構造体の各プロパティ値構造 **を割り当てる**。 
  
Address **が大** きい **ADRLIST** 構造体を返す必要がある場合、または  _lppAdrList_ に NULL を渡した場合 **、Address** は元の構造を解放し、新しい構造体を割り当てる必要があります。 **また、アドレス** は **ADRLIST** 構造に追加のプロパティ値構造を割り当て、必要に応じて古いプロパティ値構造を解放します。 **ADRLIST** 構造体のメモリを管理する方法の詳細については [、「ADRLIST および SRowSet 構造体](managing-memory-for-adrlist-and-srowset-structures.md)のメモリの管理」を参照してください。
  
 **アドレス** は _、lpAdrParms_ パラメーター DIALOG_SDI **ADRPARM** 構造体にフラグが設定されている場合、すぐに返されます。 
  
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


[ADRLIST および SRowSet 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)

