---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a727173aa1a607e878170fb4f29374cdf3fb52ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551394"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの現在のビュー コンテキストを返します。 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>パラメーター

 _ppViewContext_
  
> [out]フォームのビュー コンテキストへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームの現在のビュー コンテキストが正常に返されました。 
    
S_FALSE 
  
> フォームのビュー コンテキストはありません。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **GetViewContext** を呼び出して [、IMAPIForm::SetViewContext](imapiform-setviewcontext.md)への以前の呼び出しで確立されたビュー コンテキストへのポインターを取得します。 **SetViewContext** に対して以前に呼び出しが行われた場合 **、GetViewContext は ppViewContext** _を NULL に_ 設定します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_ppViewContext_ パラメーターで呼び出し元のフォーム ビューアーによって渡されたポインターに、フォームのビュー コンテキスト ポインターをコピーします。 フォームにビュー コンテキストがない場合は  _、ppViewContext を NULL に_ 設定します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI は **IMAPIForm::GetViewContext** メソッドを使用して、フォームにビュー コンテキストが含されているかどうかを確認します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

