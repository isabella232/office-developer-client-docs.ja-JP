---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ae2e03464ec60392d6d8afaf008f6f38d46cf9a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580000"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのビュー コンテキストを確立します。 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>パラメーター

 _pViewContext_
  
> [in]フォームの新しいビュー コンテキストへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ビュー コンテキストが正常に設定されました。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIForm::SetViewContext** メソッドを呼び出して、特定のフォーム ビュー コンテキストを現在の形式として確立します。 フォームには、一度に 1 つのビュー コンテキストのみを含めできます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

ほとんどのフォーム サーバーは、 **次のアルゴリズムを使用して SetViewContext** を実装します。 
  
- フォームのビュー コンテキストが既に存在する場合は _、pmnvs_ パラメーターで [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) メソッドを null で呼び出してフォームの登録を取り消し、ビュー コンテキストの [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して参照カウントをデクメントします。 
    
- 新しいビュー コンテキストがnull ではない場合は _、pViewContext_ パラメーターを使用して **IMAPIViewContext::SetAdviseSink** を呼び出して、新しいビューアアドバイス シンクを設定します。 
    
- 新しいビュー コンテキストが **null** ではない場合は [、IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) メソッドを呼び出して、設定されている状態フラグを決定します。 
    
- 新しいビュー コンテキストが **null** ではない場合は、それを格納し、 [その IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) メソッドを呼び出して参照カウントを増やします。 
    
- ビュー コンテキストに依存するユーザー インターフェイス要素を更新します。 
    
**IMAPIViewContext::GetViewStatus** から返される状態フラグに応じて **、SetViewContext** は他のアクションも実行できます。 たとえば、VCSTATUS_NEXTフラグVCSTATUS_PREV場合 **、SetViewContext** は新しいビュー コンテキストの [次へ] ボタンと[前へ] ボタンを有効にできます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI は **IMAPIForm::SetViewContext** メソッドを使用して、フォームが表示される前にフォームに MFCMAPI のビュー コンテキストを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

