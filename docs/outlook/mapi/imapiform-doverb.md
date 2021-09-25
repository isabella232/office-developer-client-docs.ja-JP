---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 91c78852092e6f6de9d64574e0b8369a63f6d3a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596317"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが特定の動詞に関連付けるタスクを実行する要求。
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a>パラメーター

 _iVerb_
  
> [in]フォームの動詞の 1 つに関連付けられている番号。
    
 _lpViewContext_
  
> [in]ビュー コンテキスト オブジェクトへのポインター。 _lpViewContext パラメーター_ には null を **指定できます**。
    
 _hwndParent_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 ダイアログ  _ボックスまたはウィンドウが_ モーダルではない場合 **、hwndParent** パラメーターは null である必要があります。 
    
 _lprcPosRect_
  
> [in]フォームのウィンドウのサイズと位置を含む Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 動詞が正常に呼び出されました。
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> _iVerb_ パラメーターで表される動詞は有効ですが、フォームは現在関連付けられている操作を実行できません。 
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIForm::D oVerb** メソッドを呼び出して、フォームがサポートする各動詞に関連付けるタスクをフォームが実行します。 
  
サポートされている各動詞は _、iVerb_ パラメーターで **DoVerb** に渡される数値で識別されます。 DoVerb の一般的な実装には、フォームの **iVerb** パラメーターに対して有効な値をテストする _スイッチ_ ステートメントが含まれます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォーム ビューアーが _lpViewContext_ パラメーターでビュー コンテキストを指定する場合は [、IMAPIForm::SetViewContext](imapiform-setviewcontext.md)メソッドへの以前の呼び出しで渡されたビュー コンテキストではなく **、DoVerb** 実装で使用します。 内部データ構造に必要な変更を加え、ビュー コンテキストを保存しない。 
  
DoVerb 実装で次の **タスクを実行** します。 
  
- _iVerb_ パラメーターに関連付けられている特定の動詞に必要なコードを実行します。 
    
- 必要に応じて、元のビュー コンテキストを復元します。
    
- 不明な動詞番号が渡された場合は、次のMAPI_E_NO_SUPPORT。 それ以外の場合は、実行された動詞の成功または失敗に基づいて結果を返します。
    
- フォームを閉じます。 **DoVerb** 呼び出しの完了後にフォームを閉じるのは常にユーザーの責任です。 
    
Print などの一部の動詞は **、DoVerb** 呼び出しに関してモーダルである必要があります。つまり **、DoVerb** 呼び出しが返される前に、指定された操作を完了する必要があります。 
  
フォームのウィンドウ **で使用される RECT** 構造を取得するには [、GetWindowRect 関数を呼び出](https://msdn.microsoft.com/library/ms633519) します。 
  
ハンドルを  _hwndParent_ パラメーターに保存しないのは、通常は **DoVerb** が完了するまで有効なままですが、呼び出しが戻った直後に破棄される可能性があるからです。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

モーダル以外の動詞をモーダル 動詞として機能させるには [、imapIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドから VCSTATUS_MODAL フラグを返すビュー コンテキスト実装を _lpViewContext_ をポイントします。 
  
MAPI の動詞の詳細については、「Form [Verbs」を参照してください](form-verbs.md)。 OLE での動詞の処理方法の詳細については [、「OLE とデータ転送」を参照してください](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI は **IMAPIForm::D oVerb** メソッドを使用して、フォーム上で動詞を呼び出します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[フォーム動詞](form-verbs.md)

