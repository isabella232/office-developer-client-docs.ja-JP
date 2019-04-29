---
title: iaddrbookaddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407908"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[Outlook アドレス帳] ダイアログボックスを表示します。 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>パラメーター

 _l出 uiparam_
  
> [入力]ダイアログボックスの親ウィンドウのハンドルへのポインター。 入力時には、ウィンドウハンドルを常に渡す必要があります。 出力では、 _lpadrparms_パラメーターの**ulflags**メンバーが DIALOG_SDI に設定されている場合、モードレスダイアログボックスのウィンドウハンドルが返されます。 注釈を参照してください。 
    
 _lpadrparms_
  
> [入力][アドレス] ダイアログボックスの表示と動作を制御する[ADRPARM](adrparm.md)構造体へのポインター。 
    
 _lppadrlist_
  
> [入力]受信者の情報を含む[adrlist](adrlist.md)構造体へのポインターへのポインター。 入力時には、このパラメーターを NULL にしたり、有効なポインターをポイントしたりすることができます。 出力では、このパラメーターは有効な受信者情報へのポインターを指します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> [共通アドレス] ダイアログボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

_lpadrparms_パラメーターの**ulflags**メンバーが DIALOG_SDI に設定されている場合、出力時にモードレスダイアログボックスのウィンドウハンドルの戻り値を予測します。これは Outlook では無視されます。ダイアログのモーダルバージョンは常に、Outlook 以外のクライアントに表示されます。 
  
_lppadrlist_パラメーターを使用して、MAPI によって発信者に渡された**adrlist**構造体には、各受信者に対応する1つの[adrlist](adrentry.md)構造の配列が含まれています。 _lpMods_パラメーターの送信メッセージの[IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドに渡されると、 **adrlist**構造を使用して、その受信者リストを更新できます。 
  
**adrentry**構造体内の各**adrentry**構造には、0個以上の[spropvalue](spropvalue.md)構造体、および受信者のすべてのプロパティセットに対する1つの構造が含まれています。 **Address**メソッドによって提供されるダイアログボックスを使用して受信者を削除する場合は、ゼロの**spropvalue**構造が可能です。 1つ以上の**spropvalue**構造体がある場合は、対応する**adrentry**構造を使用して、受信者を追加または更新します。 受信者を解決できます。これは、 **spropvalue**構造の1つが、受信者の**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティ、または未解決であることを示しています。これは、 **PR_ENTRYID**プロパティがれ. 
  
**PR_ENTRYID**に加えて、解決された受信者には次のプロパティが含まれています。
  
- **PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
発信者が渡す**adrlist**構造は、MAPI が返す構造体のサイズと異なる場合があります。 MAPI がより大きな**adrlist**構造を返す必要がある場合は、元の構造を解放して新しい構造を割り当てます。 **adrlist**構造体のメモリを割り当てるときは、各**spropvalue**構造体のメモリを個別に割り当てます。 **adrlist**構造体の割り当ておよび解放方法の詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。
  
 DIALOG_SDI フラグが_lpadrparms_パラメーターの**ADRPARM**構造の**ulflags**メンバーで設定されている場合は、すぐに**アドレス**が返されます。 Outlook 以外のクライアントでは、DIALOG_SDI フラグは無視されます。 DIALOG_SDI が無視される場合は、ダイアログのモーダルバージョンが表示され、ハンドルへのポインターは_lアウト uiparam_では想定されません。
  
 **Address**は**ADRPARM**構造で unicode 文字列をサポートしています。 _lpadrparms_パラメーターの**ADRPARM**の**ulflags**メンバーで AB_UNICODEUI が指定されており、それが unicode**文字列をサポートしている場合adrlist**。 Unicode 文字列は、Outlook の [アドレス帳] ダイアログボックスに表示される前に、マルチバイト文字文字列 (MBCS) 形式に変換されます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIStoreFunctions  <br/> |OpenOtherUsersMailboxFromGal  <br/> |mfcmapi は、 **Address**メソッドを使用して、開くメールボックスをユーザーが選択できるようにします。  <br/> |
   
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

