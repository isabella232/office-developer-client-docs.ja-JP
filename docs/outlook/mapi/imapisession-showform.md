---
title: imapisessionshowform
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
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335666"
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

 _uluiparam_
  
> 順番フォームの親ウィンドウへのハンドル。
    
 _lpmsgstore_
  
> 順番_lpparentfolder_パラメーターによって指定されたフォルダーを含むメッセージストアへのポインター。 
    
 _lpparentfolder_
  
> 順番_ulmessagetoken_パラメーターに関連付けられたメッセージが作成されたフォルダーへのポインター。 
    
 _lpinterface_
  
> 順番フォームに表示されるメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 _lpinterface_パラメーターは、NULL または IID_IMessage である必要があります。 NULL 結果を標準インターフェイス[IMessage](imessageimapiprop.md)で使用します。 
    
 _ulmessagetoken_
  
> 順番フォームに表示されるメッセージに関連付けられているトークン。 _ulmessagetoken_パラメーターは、以前の imapisession への呼び出しの_lアウト messagetoken_パラメーターの内容に設定する必要があります。 [:P repareform](imapisession-prepareform.md)。
    
 _lpメッセージ ent_
  
> 順番予約語NULL である必要があります。 
    
 _ulFlags_
  
> 順番メッセージを保存する方法と方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_NEW_MESSAGE 
  
> メッセージが一度も保存されていません (つまり、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されていない)。 
    
MAPI_POST_MESSAGE 
  
> メッセージは、親フォルダーに保存する必要があります。 メッセージは送信用に処理されませんが、代わりにフォルダーに投稿されます。 このフラグが設定されていない場合、メッセージは送信トレイにコピーされ、送信用に処理されます。 
    
 _ulmessagestatus_
  
> 順番_ulmessagetoken_パラメーターのトークンに関連付けられているメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。 フラグは、メッセージの状態に関する情報を提供します。 
    
 _ulmessageflags_
  
> 順番_ulmessagetoken_パラメーターのトークンに関連付けられているメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスク。 これらのフラグは、メッセージの状態に関する詳細情報を提供します。 
    
 _ulaccess_
  
> 順番フォームに表示されるメッセージのアクセス許可レベルを示すフラグ。 この情報は、 _ulmessagetoken_パラメーターのトークンに関連付けられているメッセージの**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティからコピーされます。 
    
 _lpszmessageclass_
  
> 順番フォームに表示されているメッセージのメッセージクラスへのポインター。 _ulmessagetoken_パラメーターのトークンに関連付けられているメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティからコピーします。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが正常に表示されました。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>解説

**imapisession:: showform**メソッドは、 **imapisession::P repareform**メソッドによって準備されたメッセージフォームを表示します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareForm**メソッドの_lpmessage_パラメーターで渡されるメッセージへの参照は1つだけにする必要があります。 
  
フォーム実装は、MAPI で文書化されているもの以外のエラー値を返すことができることに注意してください。 これらのエラー値を使用して、エラー条件をより正確に判断できるようにする場合は、このようにします。 それ以外の場合は、MAPI_E_CALL_FAILED を処理するのと同様に、これらのエラーを処理します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions  <br/> |openmessagemodal  <br/> |mfcmapi は、 **imapisession:: showform**メソッドを**PrepareForm**メソッドと共に使用して、モーダルフォームにメッセージを表示します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

