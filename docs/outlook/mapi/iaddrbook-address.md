---
title: IAddrBookAddress
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a13696b355e6fd815cd6bda42843505d9fc3d1f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579957"
---
# <a name="iaddrbookaddress"></a>IAddrBook::Address

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
Outlook アドレス帳] ダイアログ ボックスが表示されます。 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a>パラメーター

 _lpulUIParam_
  
> [で [チェック アウト]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。 入力、ウィンドウ ハンドルを渡す必要が常にあります。 出力、DIALOG_SDI に、 **ulFlags**のメンバー、 _lpAdrParms_パラメーターが設定されている場合は、モードレス ダイアログ ボックスのウィンドウ ハンドルが返されます。 注釈を参照してください。 
    
 _lpAdrParms_
  
> [で [チェック アウト]プレゼンテーションと、[アドレス] ダイアログ ボックスの動作を制御する[ADRPARM](adrparm.md)構造体へのポインター。 
    
 _lppAdrList_
  
> [で [チェック アウト]受信者の情報を格納する[ADRLIST](adrlist.md)構造体へのポインターへのポインター。 入力の場合、このパラメーターが NULL または有効なポインターをポイントします。 出力では、このパラメーターは、有効な受信者情報へのポインターをポイントします。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 共通のアドレス] ダイアログ ボックスが正常に表示されました。
    
## <a name="remarks"></a>注釈

Outlook では無視されます、 **ulFlags**のメンバー、 _lpAdrParms_パラメーターは、出力時に、モードレス ダイアログ ボックスのウィンドウ ハンドルの戻り値を予測し DIALOG_SDI に設定されている場合Outlook 以外のクライアントでは、モーダル ダイアログ ボックスのバージョンは常に表示します。 
  
_LppAdrList_パラメーターを通じて呼び出し元に、MAPI によって渡される**ADRLIST**構造体には、受信者ごとに 1 つの構造、 [ADRENTRY](adrentry.md)の構造体の配列が含まれています。 _LpMods_パラメーターでの送信メッセージの[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドに渡されると、その受信者のリストを更新する**ADRLIST**構造体を使用できます。 
  
**ADRLIST**構造内の個々 の**ADRENTRY**構造体には、0 個以上の[SPropValue](spropvalue.md)構造体、すべてのプロパティの設定、受信者の 1 つの構造が含まれています。 受信者を削除する**アドレス**の方法で表示されるダイアログ ボックスを使用する場合、0 **SPropValue**構造体が存在することができます。 **SPropValue**構造体が 1 つまたは複数が存在する場合、対応する**ADRENTRY**構造体を使用して、追加または受信者を更新します。 受信者を解決できるを示すこと**SPropValue**構造体のいずれかの受信者の**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティの説明、未解決の**PR_ENTRYID**プロパティがあることを示します不足しています。 
  
**PR_ENTRYID**、他は、解決の受信者には、次のプロパティが含まれます。
  
- **PR_RECIPIENT_TYPE**([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
**ADRLIST**構造で、呼び出し元に合格するには、MAPI を表す構造体のサイズが異なる可能性があります。 MAPI より大きな**ADRLIST**の構造体を返す必要がある場合に、元の構造体を解放し、新しい 1 を割り当てます。 **ADRLIST**構造体のメモリを割り当てるときに、個別に各**SPropValue**構造体のメモリを割り当てます。 割り当てるし、 **ADRLIST**構造体を解放する方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。
  
 **UlFlags** 、 **ADRPARM**構造体のメンバーに、 _lpAdrParms_パラメーターに DIALOG_SDI フラグが設定されている場合、**アドレス**はすぐに返します。 Outlook 以外のクライアントでは、DIALOG_SDI フラグは無視されます。 DIALOG_SDI は無視されますが場合、は、モーダル ダイアログ ボックスのバージョンが表示され、ハンドルへのポインターは、 _lpulUIParam_で予期しない必要があります。
  
 **アドレス**をサポートしている文字の Unicode 文字列**ADRPARM**構造体の AB_UNICODEUI は、 _lpAdrParms_パラメーターには、 **ADRPARM**の**ulFlags**メンバーで指定された**では、Unicode 文字列をサポートしている場合ADRLIST**。 Unicode 文字列は、Outlook アドレス帳] ダイアログ ボックスに表示される前に、マルチバイト文字 (MBCS) の文字列形式に変換されます。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |OpenOtherUsersMailboxFromGal  <br/> |MFCMAPI では、**アドレス**メソッドを使用して、ユーザーがどのメールボックスを開くを選択できるようにします。  <br/> |
   
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

