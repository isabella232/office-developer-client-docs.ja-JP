---
title: imapifolderdeletefolder
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
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280072"
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番削除するサブフォルダーのエントリ識別子へのポインター。
    
 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターで FOLDER_DIALOG フラグが設定されていない場合は無視されます。 
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 FOLDER_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。
    
 _ulFlags_
  
> 順番サブフォルダーの削除を制御するフラグのビットマスク。 次のフラグを設定できます。
    
DEL_FOLDERS 
  
> _lな tryid_によって参照されるサブフォルダーのすべてのサブフォルダーを削除する必要があります。 
    
DEL_MESSAGES 
  
> _lな tryid_が指すサブフォルダー内のすべてのメッセージを削除する必要があります。 
    
FOLDER_DIALOG 
  
> 操作の進行中に、進行状況のインジケーターが表示されます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定したフォルダーが正常に削除されました。
    
MAPI_E_HAS_FOLDERS 
  
> 削除されるサブフォルダーにサブフォルダーが含まれており、DEL_FOLDERS フラグが設定されていません。 サブフォルダーは削除されませんでした。
    
MAPI_E_HAS_MESSAGES 
  
> 削除されるサブフォルダーにメッセージが含まれており、DEL_MESSAGES フラグが設定されていませんでした。 サブフォルダーは削除されませんでした。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、すべてのエントリが正常に削除されませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**imapifolder::D eletefolder**メソッドは、サブフォルダーを削除します。 既定では、 **deletefolder**は空のフォルダーでのみ動作しますが、DEL_FOLDERS と DEL_MESSAGES の2つのフラグを設定することにより、空ではないフォルダーで正常に使用できます。 **deletefolder**呼び出しで DEL_FOLDERS と DEL_MESSAGES の両方のフラグを設定する、空のフォルダーまたはフォルダーのみを削除できます。 DEL_FOLDERS を使用すると、すべてのフォルダーのサブフォルダーを削除できます。DEL_MESSAGES を使用すると、フォルダーのすべてのメッセージを削除できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

削除操作に複数のフォルダーが含まれている場合は、各フォルダーで可能な限り完全に操作を実行してください。 削除するフォルダーの1つが存在しない場合や、他の場所に移動またはコピーされている場合があります。 メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件に当てはまることが予想されます。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**deletefolder**がすべてのメッセージとサブフォルダを正常に削除しました。  <br/> |S_OK  <br/> |
|**deletefolder**は、すべてのメッセージとサブフォルダを正常に削除できませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND  <br/> |
|**deletefolder**を完了できませんでした。  <br/> |MAPI_E_NOT_FOUND を除くすべてのエラー値  <br/> |
   
**deletefolder**を完了できない場合でも、作業が行われていないとは限りません。 **deletefolder**がエラーが発生する前に、1つ以上のメッセージとサブフォルダーを削除できた可能性があります。 
  
1つまたは複数のサブフォルダーを削除できない場合、 **deletefolder**は、メッセージストアプロバイダーの実装に応じて MAPI_W_PARTIAL_COMPLETION または MAPI_E_NOT_FOUND を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg  <br/> |CMsgStoreDlg:: OnDeleteSelectedItem  <br/> |mfcmapi は、 **imapifolder::D eletefolder**メソッドを使用してフォルダーを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

