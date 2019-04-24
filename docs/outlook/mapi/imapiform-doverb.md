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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329462"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが特定の動詞に関連付けられている任意のタスクを実行するよう要求します。
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a>パラメーター

 _iverb_
  
> 順番フォームの動詞の1つに関連付けられた番号。
    
 _lpviewcontext_
  
> 順番ビューコンテキストオブジェクトへのポインター。 _lpviewcontext_パラメーターは**null**にすることができます。
    
 _hwndParent_
  
> 順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。 ダイアログボックスまたはウィンドウがモーダルでない場合は、 _hwndParent_パラメーターを**null**に設定する必要があります。 
    
 _lprcPosRect_
  
> 順番フォームのウィンドウのサイズと位置を含む Win32 [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx)構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 動詞が正常に起動されました。
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> _iverb_パラメーターで表される動詞は有効ですが、フォームは現在関連付けられている操作を実行できません。 
    
## <a name="remarks"></a>解説

フォームビューアーは、 **imapiform::D overb**メソッドを呼び出して、フォームがサポートする各動詞と関連付けられているタスクをフォームが実行するように要求します。 
  
サポートされている各動詞は、 _iverb_パラメーターで**DoVerb**に渡される数値で識別されます。 **DoVerb**の通常の実装には、フォームの_iverb_パラメーターに対して有効な値をテストする**switch**ステートメントが含まれています。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームビューアーが_lpviewcontext_パラメーターのビューコンテキストを指定する場合は、以前に[imapiform:: setviewcontext](imapiform-setviewcontext.md)メソッドを呼び出したときに渡されたビューコンテキストではなく、 **DoVerb**の実装で使用します。 内部データ構造に必要な変更を加え、ビューコンテキストは保存しません。 
  
**DoVerb**の実装で、次のタスクを実行します。 
  
- _iverb_パラメーターに関連付けられている特定の動詞に必要な任意のコードを実行します。 
    
- 必要に応じて、元のビューコンテキストを復元します。
    
- 不明な動詞番号が渡された場合は、MAPI_E_NO_SUPPORT を返します。 それ以外の場合は、実行されたすべての動詞の成功または失敗に基づいて結果を返します。
    
- フォームを閉じます。 **DoVerb**の呼び出しが完了した後は、常にフォームを閉じることが責任です。 
    
Print などの一部の動詞は**DoVerb**呼び出しに関してモーダルである必要があります。つまり、 **DoVerb**呼び出しが戻る前に、指定された操作を完了する必要があります。 
  
フォームのウィンドウで使用される**RECT**構造を取得するには、 [getwindowrect](https://msdn.microsoft.com/library/ms633519)関数を呼び出します。 
  
_hwndParent_パラメーターにハンドルを保存しないでください。ただし、通常は**DoVerb**が完了するまで有効なままですが、呼び出しの戻り時に直ちに破棄することができます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[imapiviewcontext:: getviewstatus](imapiviewcontext-getviewstatus.md)メソッドから VCSTATUS_MODAL フラグを返すビューコンテキスト実装に_lpviewcontext_を指定することにより、非モーダル動詞をモーダル動詞として動作させることができます。 
  
MAPI での動詞の詳細については、「 [Form verb](form-verbs.md)」を参照してください。 ole での動詞の処理方法の詳細については、「 [ole とデータ転送](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: CallDoVerb  <br/> |mfcmapi は、 **imapiform::D overb**メソッドを使用して、フォーム上の動詞を呼び出します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[フォームの動詞](form-verbs.md)

