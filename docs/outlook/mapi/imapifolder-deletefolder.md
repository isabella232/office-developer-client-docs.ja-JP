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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417407"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]削除するサブフォルダーのエントリ識別子へのポインター。
    
 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター FOLDER_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ で FOLDER_DIALOGフラグが設定されていない限り無視されます。
    
 _ulFlags_
  
> [in]サブフォルダーの削除を制御するフラグのビットマスク。 次のフラグを設定できます。
    
DEL_FOLDERS 
  
> _lpEntryID_ が指すサブフォルダーのすべてのサブフォルダーを削除する必要があります。 
    
DEL_MESSAGES 
  
> _lpEntryID_ が指すサブフォルダー内のすべてのメッセージを削除する必要があります。 
    
FOLDER_DIALOG 
  
> 操作の進行中に進行状況インジケーターが表示されます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したフォルダーが正常に削除されました。
    
MAPI_E_HAS_FOLDERS 
  
> 削除されるサブフォルダーにはサブフォルダーが含まれているので、DEL_FOLDERSフラグは設定されません。 サブフォルダーは削除されません。
    
MAPI_E_HAS_MESSAGES 
  
> 削除されるサブフォルダーにはメッセージが含まれますが、DEL_MESSAGESフラグは設定されません。 サブフォルダーは削除されません。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのエントリが正常に削除されたという訳ではありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::D eleteFolder メソッドは** サブフォルダーを削除します。 既定では **、DeleteFolder** は空のフォルダーでのみ動作しますが、空でないフォルダーでは、DEL_FOLDERS と DEL_MESSAGES の 2 つのフラグを設定することで、このフォルダーを正常に使用できます。 **DeleteFolder** 呼び出しでDEL_FOLDERSとDEL_MESSAGES両方を設定する空のフォルダーまたはフォルダーのみを削除できます。 DEL_FOLDERSフォルダーのすべてのサブフォルダーを削除できます。DEL_MESSAGESフォルダーのすべてのメッセージを削除できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

削除操作に複数のフォルダーが含まれる場合は、フォルダーごとに可能な限り完全に操作を実行します。 削除するフォルダーの 1 つが存在しないか、他の場所に移動またはコピーされている場合があります。 メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件下で期待してください。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**DeleteFolder は** 、すべてのメッセージとサブフォルダーを正常に削除しました。  <br/> |S_OK  <br/> |
|**DeleteFolder** は、すべてのメッセージとサブフォルダーを正常に削除できなかった。  <br/> |MAPI_W_PARTIAL_COMPLETIONまたはMAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** を完了できなかった。  <br/> |エラー以外のエラー MAPI_E_NOT_FOUND  <br/> |
   
**DeleteFolder を** 完了できない場合は、作業が完了していないと見なす必要はありません。 **DeleteFolder は** 、エラーが発生する前に 1 つ以上のメッセージとサブフォルダーを削除できた可能性があります。 
  
1 つ以上のサブフォルダーを削除できない場合 **、DeleteFolder** はメッセージ ストア プロバイダーの実装に応じて、MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI は **IMAPIFolder::D eleteFolder** メソッドを使用してフォルダーを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

