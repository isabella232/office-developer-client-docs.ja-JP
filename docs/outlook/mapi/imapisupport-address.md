---
title: IMAPISupportAddress
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cb683178a8e258f571cbc3d05a3b030481905433
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800722"
---
# <a name="imapisupportaddress"></a>IMAPISupport::Address

  
  
**適用対象**: Outlook 
  
共通のアドレス] ダイアログ ボックスが表示されます。 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>パラメーター

 _lpulUIParam_
  
> [で [チェック アウト]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。 入力、ウィンドウ ハンドルを渡す必要が常にあります。 出力、DIALOG_SDI フラグは、 _lpAdrParms_パラメーターで指定された[ADRPARM](adrparm.md)構造体に設定されている場合は、モードレス ダイアログ ボックスのウィンドウ ハンドルが返されます。 
    
 _lpAdrParms_
  
> [で [チェック アウト]プレゼンテーションと、[アドレス] ダイアログ ボックスの動作を制御する**ADRPARM**構造体へのポインター。 
    
 _lppAdrList_
  
> [で [チェック アウト]アドレス一覧へのポインターへのポインター。 入力でこのリストは、いずれかのメッセージ内の受信者の現在のリストまたは NULL の場合、このようなリストが存在しない場合。 出力では、 _lppAdrList_は、最新のメッセージの受信者の一覧をポイントします。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> [アドレス] ダイアログ ボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーのサポート オブジェクトの**IMAPISupport::Address**メソッドを実装します。 アドレス帳プロバイダーは、メッセージの受信者の一覧を作成または**アドレス**を呼び出します。 
  
各受信者は、 _lppAdrList_パラメーターで指定された[ADRLIST](adrlist.md)構造体に含まれる[ADRENTRY](adrentry.md)構造体の説明です。 **ADRENTRY**構造体には、受信者のプロパティの値のうちの 1 つは、受信者の種類、または**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティの配列が含まれています。 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)への呼び出しで、 _lpMods_のパラメーターとして使用するクライアントには、この**ADRLIST**の構造体を渡すことができます。
  
**ADRLIST**構造体の各受信者も解決できるを示すこと、プロパティの値のいずれかの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティは、未解決の**PR_ENTRYID**プロパティがあることを示します不足しています。 
  
**PR_ENTRYID**、他は、解決の受信者には、次のプロパティが含まれます。
  
- **PR_RECIPIENT_TYPE**
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
未解決の受信者には、通常、 **PR_DISPLAY_NAME**と**PR_RECIPIENT_TYPE**のみが含まれます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ADRLIST**構造で、呼び出し元に合格するには、MAPI を表す構造体のサイズが異なる可能性があります。 **ADRLIST**構造体のメモリを割り当てるときに、個別に各[SPropValue](spropvalue.md)構造体のメモリを割り当てます。 
  
メモリを割り当てるには、MAPI のメモリ割り当て関数、 [ABProviderInit](abproviderinit.md)関数に渡されたポインターを使用します。 **ADRLIST**と**ADRLIST**内の**ADRENTRY**構造体の各プロパティ値の構造体の[MAPIAllocateBuffer](mapiallocatebuffer.md)関数を使用してメモリを割り当てます。 
  
**アドレス**より大きな**ADRLIST**構造体を返す必要がある場合、または_lppAdrList_に NULL を渡した場合は、**アドレス**は元の構造体を解放し、新しい 1 つを割り当てます。 **アドレス**は、 **ADRLIST**構造体に追加のプロパティ値の構造体を割り当てし、必要に応じて古いものを解放します。 **ADRLIST**構造体のメモリを管理する方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。
  
 _LpAdrParms_パラメーターに**ADRPARM**構造体に DIALOG_SDI フラグが設定されている場合、**アドレス**はすぐに返します。 
  
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


[ADRLIST および SRowSet 構造のためのメモリ管理](managing-memory-for-adrlist-and-srowset-structures.md)

