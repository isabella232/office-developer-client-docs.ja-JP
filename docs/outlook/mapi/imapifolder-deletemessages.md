---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2f2066ec582b02f92cc17586bdecc7411d847987
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580007"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上のメッセージを削除します。
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpMsgList_
  
> [in]削除するメッセージ [の数](entrylist.md) と、メッセージを識別する ENTRYID 構造体の配列を含む [ENTRYLIST](entryid.md) 構造体へのポインター。 
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター MESSAGE_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ パラメーター MESSAGE_DIALOGフラグが設定されていない限り、無視されます。 
    
 _ulFlags_
  
> [in]メッセージの削除方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
DELETE_HARD_DELETE
  
> ソフト削除されたメッセージを含むすべてのメッセージを完全に削除します。
    
MESSAGE_DIALOG 
  
> 操作が進むにつれて進行状況インジケーターが表示されます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したメッセージまたはメッセージが正常に削除されました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのメッセージが正常に削除されたというのではありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::D eleteMessages** メソッドは、フォルダーからメッセージを削除します。 存在しないメッセージ、他の場所に移動されたメッセージ、読み取り/書き込み権限で開いているメッセージ、または現在送信されているメッセージは削除できません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

削除操作に複数のメッセージが含まれる場合は、1 つ以上のメッセージを削除できない場合でも、フォルダーごとに可能な限り完全に操作を実行します。 メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件下で期待してください。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**DeleteMessages は** 、すべてのメッセージを正常に削除しました。  <br/> |S_OK  <br/> |
|**DeleteMessages は** 、すべてのメッセージとサブフォルダーを正常に削除できなかった。  <br/> |MAPI_W_PARTIAL_COMPLETIONまたはMAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** を完了できません。  <br/> |エラー以外のエラー MAPI_E_NOT_FOUND  <br/> |
   
**DeleteMessages を** 完了できない場合は、作業が完了していないと想定しません。 **DeleteMessages は** 、エラーが発生する前に 1 つ以上のメッセージを削除できた可能性があります。 
  
 **DeleteMessages は** 、メッセージ MAPI_W_PARTIAL_COMPLETIONのMAPI_E_NOT_FOUNDに応じて、この値を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI は **IMAPIFolder::D eleteMessages** メソッドを使用して、指定したメッセージを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)

