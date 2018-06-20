---
title: IMsgStoreGetReceiveFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolder
api_type:
- COM
ms.assetid: ccd9d623-a3cb-4e66-9649-78c3887cb726
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f58bd8499b63bcd526906f78143b76092f194cb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800996"
---
# <a name="imsgstoregetreceivefolder"></a>IMsgStore::GetReceiveFolder

  
  
**適用されます**: Outlook 
  
または、指定したメッセージ クラスの既定値として受信したメッセージの送信先には、メッセージ ストアのフォルダーが表示されるように設定されているフォルダーを取得します。
  
```cpp
HRESULT GetReceiveFolder(
  LPSTR lpszMessageClass,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID,
  LPSTR FAR * lppszExplicitClass
);
```

## <a name="parameters"></a>Parameters

 _lpszMessageClass_
  
> [in]受信フォルダーに関連付けられているメッセージ クラスへのポインター。 返します_lpszMessageClass_パラメーターが NULL または空の文字列を**GetReceiveFolder**に設定、既定ではメッセージ ストアのフォルダーが表示されます。 
    
 _ulFlags_
  
> [in]渡されると、返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> メッセージ クラスの文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のメッセージ クラスの文字列です。
    
 _lpcbEntryID_
  
> [out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppEntryID_
  
> [out]要求されたエントリの識別子へのポインターへのポインターでは、フォルダーが表示されます。
    
 _lppszExplicitClass_
  
> [out]として明示的に設定するメッセージ クラスへのポインターへのポインターの_lppEntryID_で指定されたフォルダーのフォルダーが表示されます。 このメッセージ クラスでは、 _lpszMessageClass_パラメーターにクラスまたはそのクラスの基本クラスと同じする必要がありますか。 NULL を渡すことは、 _lppEntryID_が指すフォルダーは、既定値には、メッセージ ストアのフォルダーが表示されることを示します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 受信フォルダーが正常に返されました。
    
## <a name="remarks"></a>備考

**IMsgStore::GetReceiveFolder**メソッドは、特定のメッセージ クラスのメッセージを受信する指定されたフォルダー、受信フォルダーのエントリ id を取得します。 呼び出し元が_lpszMessageClass_パラメーターでは、メッセージ クラスまたは NULL を指定できます。 _LpszMessageClass_が NULL の場合は、 **GetReceiveFolder**は、次の値を返します。 
  
- _LppszExplicitClass_、メッセージ クラスの 1 つ目の基本クラスの名前で示される_lpszMessageClass_は、受信フォルダーを明示的に設定します。 
    
- _LppEntryID_、基本クラスの受信フォルダーのエントリ id は、 _lppszExplicitClass_パラメーターを参照できます。 
    
たとえば、メッセージ クラス IPM の**の受信フォルダーがあるとします。注**が設定されているエントリに、受信トレイと**GetReceiveFolder**の識別子と呼ばれる_lpszMessageClass_ **IPM に設定の内容とします。Note.Phone**。 場合**IPM。Note.Phone**はありませんが、明示的な受信フォルダー セット、 **GetReceiveFolder**は、 _lppEntryID_と**IPM で、[受信トレイ] のエントリ id を返します。注** _lppszExplicitClass_にします。
  
_LppszExplicitClass_は長さ 0 の文字列、Unicode 形式で文字列またはかどうかによって、ANSI 形式の文字列のいずれかのクライアントは、メッセージ クラスの**GetReceiveFolder**を呼び出すし、そのメッセージ クラス用の受信フォルダーを設定していない、する場合、クライアントは、 _ulFlags_パラメーターに MAPI_UNICODE フラグを設定します。 
  
既定では、 _lpszMessageClass_パラメーターに NULL を渡すことによって取得したフォルダーが表示される、メッセージ ・ ストアごとに常に存在します。 
  
クライアントは、そのエントリの識別子を保持するメモリを解放するのには_lppEntryID_で返されるエントリの識別子を使用して登録が完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出す必要があります。 **MAPIFreeBuffer**は、その文字列を保持しているメモリを解放するのには_lppszExplicitClass_で返されるメッセージ クラスの文字列の処理が終わったらそれも呼び出す必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetInbox  <br/> |MFCMAPI では、 **IMsgStore::GetReceiveFolder**メソッドを使用して、受信トレイ フォルダーに移動します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

