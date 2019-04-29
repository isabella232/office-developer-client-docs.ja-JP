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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426073"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数のメッセージを削除します。
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpmsglist_
  
> 順番削除するメッセージ数、およびメッセージを識別する[ENTRYID](entryid.md)構造体の配列を含む[entrylist](entrylist.md)構造体へのポインター。 
    
 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターで MESSAGE_DIALOG フラグが設定されていない場合は無視されます。 
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 MESSAGE_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。 
    
 _ulFlags_
  
> 順番メッセージを削除する方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
DELETE_HARD_DELETE
  
> 削除されたものを含むすべてのメッセージを完全に削除します。
    
MESSAGE_DIALOG 
  
> 操作の進行状況を示すインジケーターを表示します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したメッセージまたはメッセージが正常に削除されました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのメッセージが正常に削除されませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>注釈

**imapifolder::D eletemessages**メソッドは、フォルダーからメッセージを削除します。 存在しないメッセージ、他の場所に移動したメッセージ、読み取り/書き込みアクセス許可で開いているメッセージ、または現在送信されているメッセージは削除できません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

削除操作に複数のメッセージが含まれている場合は、1つ以上のメッセージを削除できない場合でも、フォルダーごとにできるだけ完全に操作を実行してください。 メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件に当てはまることが予想されます。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**DeleteMessages**はすべてのメッセージを正常に削除しました。  <br/> |S_OK  <br/> |
|**DeleteMessages**は、すべてのメッセージとサブフォルダーを正常に削除できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages**を完了できませんでした。  <br/> |MAPI_E_NOT_FOUND を除くすべてのエラー値  <br/> |
   
**DeleteMessages**が完了できない場合は、作業が行われていないことを前提としていません。 エラーが発生する前に、 **DeleteMessages**は1つ以上のメッセージを削除できた可能性があります。 
  
 **DeleteMessages**は、メッセージストアの実装に応じて、MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|folderdlg  <br/> |cfolderdlg:: OnDeleteSelectedItem  <br/> |mfcmapi は、 **imapifolder::D eletemessages**メソッドを使用して、指定されたメッセージを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)

