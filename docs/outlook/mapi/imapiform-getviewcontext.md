---
title: imapiformgetviewcontext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329461"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの現在のビューコンテキストを返します。 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>パラメーター

 _ppviewcontext_
  
> 読み上げフォームのビューコンテキストへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームの現在のビューコンテキストが正常に返されました。 
    
S_FALSE 
  
> フォームにビューコンテキストはありません。
    
## <a name="remarks"></a>解説

フォーム閲覧者は**getviewcontext**を呼び出して、以前の[imapiform:: setviewcontext](imapiform-setviewcontext.md)への呼び出しで設定されたビューコンテキストへのポインターを取得します。 **setviewcontext**に対して前回の呼び出しが行われていない場合、 **getviewcontext**は_ppviewcontext_を NULL に設定します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームのビューコンテキストポインターを、 _ppviewcontext_パラメーターの呼び出し元フォームビューアーによって渡されるポインターにコピーします。 フォームにビューコンテキストがない場合は、 _ppviewcontext_を NULL に設定します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions  <br/> |openmessagenonmodal  <br/> |mfcmapi は、 **imapiform:: getviewcontext**メソッドを使用して、フォームにビューコンテキストがあるかどうかを確認します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

