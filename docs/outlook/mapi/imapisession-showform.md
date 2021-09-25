---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbe1087c2d7036aeb7b02b019cf6bec84e43d139
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561531"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームを表示します。
  
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
  
> [in]  _lpParentFolder_ パラメーターが指すフォルダーを含むメッセージ ストアへのポインター。 
    
 _lpParentFolder_
  
> [in]  _ulMessageToken_ パラメーターに関連付けられたメッセージが作成されたフォルダーへのポインター。 
    
 _lpInterface_
  
> [in]フォームに表示されるメッセージにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lpInterface パラメーターは_ NULL または null IID_IMessage。 NULL を渡す場合、標準インターフェイス [IMessage](imessageimapiprop.md)が使用されます。 
    
 _ulMessageToken_
  
> [in]フォームに表示するメッセージに関連付けられているトークン。 _ulMessageToken_ パラメーターは、前の呼び出しから [IMAPISession::P repareForm](imapisession-prepareform.md)への _lpulMessageToken_ パラメーターの内容に設定する必要があります。
    
 _lpMessageSent_
  
> [in]予約済み。NULL である必要があります。 
    
 _ulFlags_
  
> [in]メッセージの保存方法と保存方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NEW_MESSAGE 
  
> メッセージが保存されたことがない ( [つまり、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドが呼び出されたことがない)。 
    
MAPI_POST_MESSAGE 
  
> メッセージは親フォルダーに保存する必要があります。 メッセージは送信用に処理されませんが、代わりにフォルダーに投稿されます。 このフラグが設定されていない場合、メッセージは送信ボックスにコピーされ、送信用に処理されます。 
    
 _ulMessageStatus_
  
> [in]_ulMessageToken_ パラメーター内のトークンに **関連付けられた** メッセージの PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。 フラグは、メッセージの状態に関する情報を提供します。 
    
 _ulMessageFlags_
  
> [in]_ulMessageToken_ パラメーター内のトークン **に関連付** けられているメッセージの PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。 これらのフラグは、メッセージの状態に関する詳細な情報を提供します。 
    
 _ulAccess_
  
> [in]フォームに表示されるメッセージのアクセス許可レベルを示すフラグ。 この情報は _、ulMessageToken_ パラメーター **PR_ACCESS** に関連付けられたメッセージの PR_ACCESS ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティからコピーされます。 
    
 _lpszMessageClass_
  
> [in]_ulMessageToken_ パラメーター内のトークンに関連付けられたメッセージの **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティからコピーされた、フォームに表示されるメッセージのメッセージ クラスへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが正常に表示されました。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
## <a name="remarks"></a>注釈

**IMAPISession::ShowForm** メソッドは **、IMAPISession::P repareForm** メソッドによって準備されたメッセージ フォームを表示します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

PrepareForm メソッドの _lpMessage_ パラメーターで渡されるメッセージへの参照は **1** つのみです。 
  
フォームの実装では、MAPI で文書化されているエラー値以外のエラー値を返す可能性があります。 これらのエラー値を使用してエラー状態をより正確に判断できる場合は、これを行います。 それ以外の場合は、これらのエラーを処理する場合と同じようにMAPI_E_CALL_FAILED。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI は **IMAPISession::ShowForm** メソッドを **PrepareForm** メソッドと共に使用して、モーダル 形式でメッセージを表示します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

