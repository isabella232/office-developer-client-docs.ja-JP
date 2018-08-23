---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e9e0ad958acc40dd28f3d9aab9996c1b7a36f38a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591486"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームが表示されます。
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]フォームの親ウィンドウへのハンドル。
    
 _lpMsgStore_
  
> [in]_LpParentFolder_パラメーターが指すフォルダーが含まれるメッセージ ・ ストアへのポインターです。 
    
 _lpParentFolder_
  
> [in]_UlMessageToken_パラメーターに関連付けられているメッセージが作成されたフォルダーへのポインター。 
    
 _lpInterface_
  
> [in]フォームに表示されるメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _LpInterface_パラメーターは、NULL または IID_IMessage である必要があります。 NULL を渡すことは、標準的なインタ フェース、 [IMessage](imessageimapiprop.md)、使用中になります。 
    
 _ulMessageToken_
  
> [in]フォームに表示されるメッセージに関連付けられているトークンです。 [IMAPISession::PrepareForm](imapisession-prepareform.md)の以前の呼び出しからは、 _lpulMessageToken_パラメーターの内容を_ulMessageToken_パラメーターを設定しなければなりません。
    
 _lpMessageSent_
  
> [in]予約されています。NULL である必要があります。 
    
 _ulFlags_
  
> [in]メッセージを保存する方法とするかどうかを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_NEW_MESSAGE 
  
> メッセージが保存されていない (つまり、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドはそのことはありませんが呼び出されました)。 
    
MAPI_POST_MESSAGE 
  
> メッセージは、その親フォルダーに保存する必要があります。 メッセージを送信するのには処理されませんが、代わりに、フォルダーに投稿します。 このフラグが設定されていない場合メッセージが送信トレイにコピーされを送信するための処理します。 
    
 _ulMessageStatus_
  
> [in]_UlMessageToken_パラメーターのトークンに関連付けられたメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティからコピーしたフラグのビットマスクです。 フラグは、メッセージの状態に関する情報を提供します。 
    
 _ulMessageFlags_
  
> [in]_UlMessageToken_パラメーターのトークンに関連付けられたメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティからコピーしたフラグのビットマスクです。 これらのフラグさらに、メッセージの状態に関する情報を提供します。 
    
 _ulAccess_
  
> [in]フォームに表示されるメッセージのアクセス許可レベルを示すフラグです。 この情報は、 _ulMessageToken_パラメーターのトークンに関連付けられたメッセージの ([PidTagAccess](pidtagaccess-canonical-property.md)) である**PR_ACCESS**プロパティからコピーされます。 
    
 _lpszMessageClass_
  
> [in]**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) は、 _ulMessageToken_パラメーターのトークンに関連付けられているメッセージのコピーをフォームに表示されているメッセージのメッセージ クラスへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォームが正常に表示されました。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>注釈

**IMAPISession::ShowForm**メソッドには、 **IMAPISession::PrepareForm**メソッドによって準備されているメッセージ フォームが表示されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareForm**メソッドの_lpMessage_パラメーターで渡されたメッセージに対する単一の参照だけが必要です。 
  
フォームの実装が MAPI によって記載されているものとは別のエラー値を返すことに注意します。 これらのエラー値を使用すると、エラー状態のより正確な判断を下すため、これの操作を行います。 MAPI_E_CALL_FAILED とそれ以外の場合、これらのエラーを処理します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI では、モーダル形式でメッセージを表示するのには、 **PrepareForm**メソッドと**IMAPISession::ShowForm**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

