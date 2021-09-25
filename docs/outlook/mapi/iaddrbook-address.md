---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c4516c081fdd4cd41b1675a41d42957d6d4dd03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592474"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[アドレスOutlook] ダイアログ ボックスを表示します。 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>パラメーター

 _lpulUIParam_
  
> [in, out]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。 入力時には、ウィンドウ ハンドルを常に渡す必要があります。 出力時に _、lpAdrParms_ パラメーターの **ulFlags** メンバーが DIALOG_SDI に設定されている場合、モードレス ダイアログ ボックスのウィンドウ ハンドルが返されます。 注釈を参照してください。 
    
 _lpAdrParms_
  
> [in, out]アドレス ダイアログ ボックスの表示と動作を制御する [ADRPARM](adrparm.md) 構造体へのポインター。 
    
 _lppAdrList_
  
> [in, out]受信者情報を含む [ADRLIST](adrlist.md) 構造体へのポインター。 入力時に、このパラメーターは NULL または有効なポインターをポイントできます。 出力時に、このパラメーターは有効な受信者情報へのポインターを指します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> [共通アドレス] ダイアログ ボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

_lpAdrParms_ パラメーターの **ulFlags** メンバーが、出力時のモードレス ダイアログ ボックスのウィンドウ ハンドルの戻り値を予期して DIALOG_SDI に設定されている場合、Outlook では無視されます。モーダル バージョンのダイアログは、常にクライアント以外のクライアントOutlookされます。 
  
_LppAdrList_ パラメーターを介して呼び出し元に MAPI によって渡される **ADRLIST** 構造体には [、ADRENTRY](adrentry.md)構造体の配列が含まれています。受信者ごとに 1 つの構造です。 _lpMods_ パラメーターで送信メッセージの [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドに渡された場合 **、ADRLIST** 構造を使用して受信者リストを更新できます。 
  
ADRLIST 構造体 **内の** 各 **ADRENTRY** 構造には、受信者に設定されたプロパティごとに 1 つの構造である 0 個以上の [SPropValue](spropvalue.md) 構造体が含まれています。 Address メソッドによって表示されるダイアログ ボックスを使用して受信者を削除すると **、SPropValue** 構造体が 0 になる場合があります。 1 つ以上の **SPropValue** 構造体がある場合、対応する **ADRENTRY** 構造体を使用して受信者を追加または更新します。 受信者は解決できます。 **これは、SPropValue** 構造体の 1 つが受信者の **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティ、または未解決を表し **、PR_ENTRYID** プロパティが見つからないかどうかを示します。 
  
解決済み受信者 **には、PR_ENTRYID** に加えて、次のプロパティが含まれます。
  
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
呼 **び出し元が渡す ADRLIST** 構造は、MAPI が返す構造とは異なるサイズである可能性があります。 MAPI は、より大きな **ADRLIST** 構造を返す必要がある場合、元の構造を解放し、新しい構造を割り当てる必要があります。 **ADRLIST** 構造体のメモリを割り当てる場合は **、SPropValue** 構造体ごとに個別にメモリを割り当てる必要があります。 ADRLIST 構造体を割り当て、解放する方法の詳細については **、「ADRLIST** および SRowSet 構造体のメモリの管理」 [を参照してください。](managing-memory-for-adrlist-and-srowset-structures.md)
  
  _lpAdrParms_ パラメーター DIALOG_SDI **ADRPARM** 構造体の **ulFlags** メンバーにフラグが設定されている場合、アドレスは直ちに返します。 非DIALOG_SDIクライアントでは、このフラグはOutlookされません。 このDIALOG_SDIを無視すると、モーダル バージョンのダイアログが表示され  _、lpulUIParam_ でハンドルへのポインターを予期しない必要があります。
  
 アドレスは _、lpAdrParms_ パラメーターの ADRPARM の **ulFlags** メンバーで AB_UNICODEUI が指定されている場合 **、ADRPARM** 構造体の Unicode 文字文字列をサポートし **、ADRLIST** で Unicode 文字文字列をサポートします。  Unicode 文字列は、アドレス帳の [アドレス帳] ダイアログ ボックスに表示される前に、マルチバイト文字文字列 (MBCS) Outlook変換されます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI は **Address メソッドを使用** して、ユーザーが開くメールボックスを選択できます。  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[ADRPARM](adrparm.md)
  
[FreePadrlist](freepadrlist.md)
  
[FreeProws](freeprows.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

