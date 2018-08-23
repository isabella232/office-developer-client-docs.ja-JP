---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 287577babc9a40b771aa9917211ba5dcbf8190ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584941"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォルダー自体を削除することがなく、フォルダーからすべてのメッセージとサブフォルダーを削除します。
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。 _UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。 
    
 _ulFlags_
  
> [in]フォルダーを空にする方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
DEL_ASSOCIATED 
  
> メッセージに関連付けられているコンテンツが含まれるサブフォルダーを含めて、すべてのサブフォルダーを削除します。 DEL_ASSOCIATED フラグでは、呼び出しは最上位のフォルダーに対してのみ意味を持ちます。
    
DELETE_HARD_DELETE
  
> ソフト削除されたものも含めて、すべてのメッセージを完全に削除します。
    
FOLDER_DIALOG 
  
> 操作の進行中に進行状況のインジケーターが表示されます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォルダーが正常に空になった。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しが成功したが、フォルダーが完全に空になりません。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::EmptyFolder**メソッドは、フォルダー自体を削除することがなくすべてのフォルダーの内容を削除します。 
  
**EmptyFolder**の呼び出し、中に送信されたメッセージは削除されません。 
  
関連のフォルダーの内容には、フォームの定義を含めることも、ビュー、ルール、カスタム フォーム、およびカスタム ソリューションのストレージの説明に使用したメッセージが含まれます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

フォルダーに送信されたメッセージの[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)メソッドを呼び出さないでください。 送信されたメッセージは削除されません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

次の条件下で、これらの戻り値を期待してください。
  
|**条件**|**戻り値**|
|:-----|:-----|
|**EmptyFolder**では、フォルダーを空にしました。  <br/> |S_OK  <br/> |
|**EmptyFolder**は、完全にフォルダーを空にできませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder**は完了できませんでした。  <br/> |エラー値  <br/> |
   
**EmptyFolder**が完了することではない場合と仮定しないでその作業は実行されませんでした。 **EmptyFolder**はエラーが発生する前にフォルダーの内容の一部を削除することにされている可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI では、 **IMAPIFolder::EmptyFolder**メソッドを使用して、指定したフォルダーの内容を削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[エラー処理のためのマクロの使用](using-macros-for-error-handling.md)

