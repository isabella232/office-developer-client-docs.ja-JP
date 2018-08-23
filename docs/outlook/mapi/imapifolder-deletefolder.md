---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 02815c60b6bfc9809871af19e922913622588fc9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584318"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
サブフォルダーを削除します。
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]サブフォルダーを削除するには、エントリの識別子へのポインター。
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _UlFlags_パラメーターに FOLDER_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。 _UlFlags_に FOLDER_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。
    
 _ulFlags_
  
> [in]サブフォルダーの削除を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
DEL_FOLDERS 
  
> _LpEntryID_で指定されたサブフォルダーのすべてのサブフォルダーを削除する必要があります。 
    
DEL_MESSAGES 
  
> _LpEntryID_で指定されたサブフォルダー内のすべてのメッセージを削除する必要があります。 
    
FOLDER_DIALOG 
  
> 操作の進行中に進行状況のインジケーターが表示されます。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 指定したフォルダーが削除されました。
    
MAPI_E_HAS_FOLDERS 
  
> 削除されているサブフォルダーには、サブフォルダーが含まれていて、DEL_FOLDERS フラグが設定されませんでした。 サブフォルダーは削除されませんでした。
    
MAPI_E_HAS_MESSAGES 
  
> サブフォルダーを削除するには、メッセージが表示されて、DEL_MESSAGES フラグが設定されませんでした。 サブフォルダーは削除されませんでした。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しが成功したが、すべてのエントリが正常に削除されました。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::DeleteFolder**メソッドでは、サブフォルダーを削除します。 既定では、 **DeleteFolder**が空のフォルダーに対してのみ動作する使用することが、正常に空でないフォルダーに 2 つのフラグを設定することによって: DEL_FOLDERS と DEL_MESSAGES。 空のフォルダーまたは**DeleteFolder**の呼び出しに DEL_FOLDERS と DEL_MESSAGES の両方のフラグを設定するフォルダーのみを削除できます。 DEL_FOLDERS により、すべてのフォルダー内のサブフォルダーを削除します。DEL_MESSAGES は、すべてのフォルダーのメッセージを削除するを有効にします。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

削除操作には、複数のフォルダーが含まれているときに、できるだけ完全に各フォルダーの操作を実行します。 削除するフォルダーのいずれかの場合があります存在しないかが移動またはコピー他の場所。 メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

次の条件下で、これらの戻り値を期待してください。
  
|**条件**|**戻り値**|
|:-----|:-----|
|**DeleteFolder**は、すべてのメッセージとサブフォルダーが正常に削除されました。  <br/> |S_OK  <br/> |
|**DeleteFolder**は、正常にすべてのメッセージとサブフォルダーを削除できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder**は完了できませんでした。  <br/> |MAPI_E_NOT_FOUND を除くエラー値  <br/> |
   
**DeleteFolder**が完了することではない場合と仮定しないでその作業は実行されませんでした。 **DeleteFolder**はエラーが発生する前に 1 つまたは複数のメッセージとサブフォルダーを削除することにされている可能性があります。 
  
1 つまたは複数のサブフォルダーを削除できない場合、 **DeleteFolder**は、メッセージ ストア プロバイダーの実装によって MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI では、 **IMAPIFolder::DeleteFolder**メソッドを使用して、フォルダーを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

