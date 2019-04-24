---
title: imapiformsetviewcontext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350947"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのビューコンテキストを確立します。 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>パラメーター

 _pviewcontext_
  
> 順番フォームの新しいビューコンテキストへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ビューコンテキストが正常に設定されました。
    
## <a name="remarks"></a>解説

フォームビューアーは、 **imapiform:: setviewcontext**メソッドを呼び出して、特定のフォームビューコンテキストを current として設定します。 フォームは、一度に1つのビューコンテキストのみを持つことができます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

ほとんどのフォームサーバーは、次のアルゴリズムを使用して**setviewcontext**を実装します。 
  
- フォームのビューコンテキストが既に存在する場合は、 _pmnvs_パラメーターに**null**を指定して[imapiviewcontext:: SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出して、フォームの登録をキャンセルし、ビューコンテキストの[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)を呼び出します。メソッドは、その参照カウントをデクリメントします。 
    
- 新しいビューコンテキストが**null**でない場合は、 _pviewcontext_パラメーターを使用して**imapiviewcontext:: SetAdviseSink**を呼び出し、新しいビューアドバイズシンクを設定します。 
    
- 新しいビューコンテキストが**null**でない場合は、 [imapiviewcontext:: getviewstatus](imapiviewcontext-getviewstatus.md)メソッドを呼び出して、どの状態フラグが設定されているかを確認します。 
    
- 新しいビューコンテキストが**null**でない場合は、それを格納して、その参照カウントをインクリメントするように[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。 
    
- ビューコンテキストに依存するユーザーインターフェイス要素を更新します。 
    
**imapiviewcontext:: getviewstatus**から返されるステータスフラグによっては、 **setviewcontext**で他のアクションを実行することもできます。 たとえば、VCSTATUS_NEXT と VCSTATUS_PREV のフラグが返された場合、 **setviewcontext**は新しいビューコンテキストに対して**次**のボタンと**前**のボタンを有効にすることができます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions  <br/> |createanddisplaynewmailinfolder  <br/> |mfcmapi は、 **imapiform:: setviewcontext**メソッドを使用して、フォームが表示される前にフォーム上に mfcmapi のビューコンテキストを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

