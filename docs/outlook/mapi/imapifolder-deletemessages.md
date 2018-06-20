---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7845abc4f3010daf8e13d56ac4b13d0333bad07e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800491"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**適用されます**: Outlook 
  
1 つまたは複数のメッセージを削除します。
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMsgList_
  
> [in]削除するメッセージの数と、メッセージを識別する[エントリ ID](entryid.md)の構造体の配列を含む[ENTRYLIST](entrylist.md)構造体へのポインター。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _UlFlags_パラメーターに MESSAGE_DIALOG フラグが設定されていない限り、 _ulUIParam_パラメーターは無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。 _LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。 _UlFlags_パラメーターに MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。 
    
 _ulFlags_
  
> [in]メッセージを削除する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
DELETE_HARD_DELETE
  
> ソフト削除されたものも含めて、すべてのメッセージを完全に削除します。
    
MESSAGE_DIALOG 
  
> 操作の進行中は、進行状況のインジケーターを表示します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 指定したメッセージまたはメッセージが正常に削除されました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しが成功したが、すべてのメッセージが正常に削除されました。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

**IMAPIFolder::DeleteMessages**メソッドは、フォルダーからメッセージを削除します。 存在せず、別の場所に移動されている、読み取り/書き込み権限で開かれている、または送信される現在のメッセージを削除することはできません。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

削除操作には、複数のメッセージが含まれているときに操作を実行できるだけ完全に、フォルダーごとに 1 つまたは複数のメッセージを削除できない場合でも。 メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

次の条件下で、これらの戻り値を期待してください。
  
|**条件**|**戻り値**|
|:-----|:-----|
|**DeleteMessages**はすべてのメッセージを正常に削除します。  <br/> |S_OK  <br/> |
|**DeleteMessages**は、正常にすべてのメッセージとサブフォルダーを削除できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages**は完了できませんでした。  <br/> |MAPI_E_NOT_FOUND を除くエラー値  <br/> |
   
**DeleteMessages**が完了することではない場合と仮定しないでその作業は実行されませんでした。 **DeleteMessages**はエラーが発生する前に 1 つまたは複数のメッセージを削除することにされている可能性があります。 
  
 **DeleteMessages**は、メッセージ ストアの実装によって、MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI では、 **IMAPIFolder::DeleteMessages**メソッドを使用して、指定したメッセージを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[エントリ ID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[エラー処理のためのマクロを使用してください。](using-macros-for-error-handling.md)

