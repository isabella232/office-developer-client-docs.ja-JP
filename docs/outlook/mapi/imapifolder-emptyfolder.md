---
title: imapifolderemptyfolder
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
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280107"
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

 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。 _uluiparam_パラメーターは、 _ulflags_パラメーターで FOLDER_DIALOG フラグが設定されていない場合は無視されます。 
    
 _lpprogress_
  
> 順番進行状況インジケーターを表示する progress オブジェクトへのポインター。 _lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。 FOLDER_DIALOG フラグが_ulflags_パラメーターで設定されていない場合、 _lpprogress_パラメーターは無視されます。 
    
 _ulFlags_
  
> 順番フォルダーを空にする方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
DEL_ASSOCIATED 
  
> 関連付けられたコンテンツを含むメッセージを含むサブフォルダーを含む、すべてのサブフォルダーを削除します。 DEL_ASSOCIATED フラグは、呼び出しが作用する最上位のフォルダーに対してのみ意味があります。
    
DELETE_HARD_DELETE
  
> 削除されたものを含むすべてのメッセージを完全に削除します。
    
FOLDER_DIALOG 
  
> 操作の進行中に進行状況のインジケーターを表示します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォルダーが正常に空にされました。
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、フォルダーが完全に空になっていませんでした。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**imapifolder:: emptyfolder**メソッドは、フォルダー自体を削除せずに、フォルダーの内容をすべて削除します。 
  
**emptyfolder**を呼び出している間、送信されたメッセージは削除されません。 
  
フォルダーに関連付けられたコンテンツには、ビュー、ルール、カスタムフォーム、およびカスタムソリューションストレージを記述するために使用されるメッセージが含まれます。また、フォーム定義を含めることもできます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

送信されたフォルダー内のメッセージに対して[IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)メソッドを呼び出さないでください。 送信されたメッセージは削除されません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

これらの戻り値は、次の条件に当てはまることが予想されます。
  
|**Condition**|**戻り値**|
|:-----|:-----|
|**emptyfolder**は、フォルダーを正常に空にしました。  <br/> |S_OK  <br/> |
|**emptyfolder**はフォルダーを完全に空にすることができませんでした。  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**emptyfolder**を完了できませんでした。  <br/> |任意のエラー値  <br/> |
   
**emptyfolder**を完了できない場合は、作業が行われていないことを前提としていません。 **emptyfolder**は、エラーが発生する前にフォルダーの内容の一部を削除することができた可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MsgStoreDlg  <br/> |CMsgStoreDlg:: onemptyfolder  <br/> |mfcmapi は、 **imapifolder:: emptyfolder**メソッドを使用して、指定されたフォルダーの内容を削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[エラー処理にマクロを使用する](using-macros-for-error-handling.md)

