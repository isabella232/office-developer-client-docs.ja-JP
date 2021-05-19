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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416784"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダー自体を削除せずに、フォルダーからすべてのメッセージとサブフォルダーを削除します。
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。 _ulUIParam_ パラメーターは _、ulFlags_ パラメーター FOLDER_DIALOGフラグが設定されていない限り、無視されます。 
    
 _lpProgress_
  
> [in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。 _lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 _lpProgress パラメーター_ は _、ulFlags_ パラメーター FOLDER_DIALOGフラグが設定されていない限り、無視されます。 
    
 _ulFlags_
  
> [in]フォルダーを空にする方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
DEL_ASSOCIATED 
  
> 関連付けられたコンテンツを含むメッセージを含むサブフォルダーを含む、すべてのサブフォルダーを削除します。 このDEL_ASSOCIATEDは、呼び出しが動作するトップ レベル のフォルダーについてのみ意味を持ちます。
    
DELETE_HARD_DELETE
  
> ソフト削除されたメッセージを含むすべてのメッセージを完全に削除します。
    
FOLDER_DIALOG 
  
> 操作の進行中に進行状況インジケーターを表示します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォルダーが正常に空にされました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、フォルダーが完全に空にされたのではありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPIFolder::EmptyFolder** メソッドは、フォルダー自体を削除せずに、フォルダーのすべてのコンテンツを削除します。 
  
**EmptyFolder 呼び出し** 中に、送信されたメッセージは削除されません。 
  
フォルダーに関連付けられたコンテンツには、ビュー、ルール、カスタム フォーム、カスタム ソリューション ストレージを記述するために使用されるメッセージが含まれます。また、フォーム定義も含めることができます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

送信されたフォルダー内 [のメッセージに対して IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) メソッドを呼び出さない。 送信されたメッセージは削除されません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件下で期待してください。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**EmptyFolder** がフォルダーを正常に空にしました。  <br/> |S_OK  <br/> |
|**EmptyFolder** がフォルダーを完全に空にできなかった。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** を完了できません。  <br/> |エラー値  <br/> |
   
**EmptyFolder を** 完了できない場合は、作業が完了していないと想定しません。 **EmptyFolder は** 、エラーが発生する前にフォルダーのコンテンツの一部を削除できた可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI は **IMAPIFolder::EmptyFolder** メソッドを使用して、指定したフォルダーの内容を削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)

