---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398095"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームは、タスクをどのような実行要求は、特定の動作に関連付けます。
  
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
  
> [in]フォームの動作のいずれかに関連付けられている番号です。
    
 _lpViewContext_
  
> [in]ビュー コンテキスト オブジェクトへのポインター。 _LpViewContext_パラメーターを**null**にすることができます。
    
 _hwndParent_
  
> [in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。 ダイアログ ボックスまたはウィンドウがモーダルではない場合、 _hwndParent_パラメーターを**null**にする必要があります。 
    
 _lprcPosRect_
  
> [in]Win32 へのポインターのサイズと、フォームのウィンドウの位置を含む[RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx)構造体。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 動詞は正常に呼び出されました。
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> _IVerb_パラメーターによって表される動詞が有効ですが、フォームがそれに関連付けられている操作を実行できません。 
    
## <a name="remarks"></a>備考

フォームの閲覧者は、フォームがフォームをサポートしている各動詞に関連付けることのタスクを実行することを要求する**IMAPIForm::DoVerb**メソッドを呼び出します。 
  
_IVerb_パラメーターで**DoVerb**に渡される数値はそれぞれ、サポートされている識別されます。 **DoVerb**の典型的な実装には、フォームの_iVerb_パラメーターに有効な値をテストする**switch**ステートメントが含まれています。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

フォーム ビューアーは、 _lpViewContext_パラメーターで、ビューのコンテキストを指定する場合は、 [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)メソッドの以前の呼び出しに渡されるビューのコンテキストではなく、 **DoVerb**の実装に使用します。 変更を行いどのような内部データ構造体に必要なビューのコンテキストを保存できません。 
  
**DoVerb**実装では、次のタスクを実行します。 
  
- _IVerb_パラメーターに関連付けられている特定の動詞のために必要な任意のコードを実行します。 
    
- 必要に応じて、元のビュー コンテキストを復元します。
    
- 不明な動詞の数が渡された場合は、MAPI_E_NO_SUPPORT を返します。 それ以外の場合、どのような動詞の実行の成否に基づいて結果を返します。
    
- フォームを閉じます。 **DoVerb**呼び出しが完了した後、フォームを閉じる必要が常にします。 
    
印刷などのいくつかの動詞は、**これら**に対してはモーダルである必要があります-つまり、 **DoVerb**呼び出しから戻る前にした操作を完了する必要があります。 
  
フォームのウィンドウで使用されている**RECT**構造体を取得するには、[受け取り](https://msdn.microsoft.com/library/ms633519)関数を呼び出します。 
  
通常は、 **DoVerb**が完了するまで、そのことができますすぐに破棄する呼び出しの戻り値にするため、 _hwndParent_パラメーターのハンドルを保存しません。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LpViewContext_ ] をポイントして、 [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドから、VCSTATUS_MODAL フラグを返すビュー コンテキストの実装のモーダル動詞として機能する非モーダル動詞を行うことができます。 
  
MAPI での動詞の詳細については、[動詞のフォーム](form-verbs.md)を参照してください。 OLE 動詞を処理する方法の詳細については、 [OLE アプリケーションとデータの転送](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI では、 **IMAPIForm::DoVerb**メソッドを使用して、フォーム上の動詞を呼び出します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[コード サンプルとしての MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[フォームの動詞](form-verbs.md)

