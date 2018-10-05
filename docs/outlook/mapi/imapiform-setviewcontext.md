---
title: IMAPIFormSetViewContext
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384312"
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
  
> [in]フォームの新しいビューのコンテキストへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ビュー コンテキストが正常に設定されました。
    
## <a name="remarks"></a>備考

フォーム ビューアーは、現在として、特定のフォーム ビューのコンテキストを確立するために**IMAPIForm::SetViewContext**メソッドを呼び出します。 フォームでは、同時にのみ 1 つのビュー コンテキストを持つことができます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

フォームのほとんどのサーバーは、次のアルゴリズムを使用して、 **SetViewContext**を実装します。 
  
- _Pmnvs_のパラメーターに**null**に[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出すことによって、フォームの登録を取り消すし、ビュー コンテキスト[リ ス](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)を呼び出して、フォームのビューのコンテキストが既に存在する場合参照カウントをデクリメントするメソッドです。 
    
- 新しいビューのコンテキストが**null**でない場合、新しいビューを設定するのには、 _pViewContext_パラメーターを使用して、 **IMAPIViewContext::SetAdviseSink**の呼び出しは、シンクを案内します。 
    
- 新しいビューのコンテキストが**null**でない場合は、のどの状態フラグが設定されている確認するのには[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドを呼び出します。 
    
- 新しいビューのコンテキストが**null**でない場合は、格納し、その参照カウントをインクリメントするには、その[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。 
    
- ビューのコンテキストに依存するすべてのユーザー インターフェイス要素を更新します。 
    
**IMAPIViewContext::GetViewStatus**から返されるステータスのフラグに応じて、 **SetViewContext**は他のアクションも実行できます。 たとえば、VCSTATUS_NEXT および VCSTATUS_PREV のフラグが返される場合、 **SetViewContext**は新しいビュー コンテキストの**次**または**前**のボタンを有効にできます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI では、 **IMAPIForm::SetViewContext**メソッドを使用して、フォームが表示される前に、フォームの MFCMAPI のビュー コンテキストを設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

