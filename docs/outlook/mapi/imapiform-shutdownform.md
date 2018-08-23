---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9a6ab96a70bce622f44de6576e7b77861302de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800505"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**適用対象**: Outlook 
  
フォームを閉じます。
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>パラメーター

 _ulSaveOptions_
  
> [in]フォームを閉じる前にフォーム内のデータを保存するかどうか方法を制御する値です。 次のフラグのいずれかを設定できます。
    
SAVEOPTS_NOSAVE 
  
> フォーム データを保存することがありませんか。
    
SAVEOPTS_PROMPTSAVE 
  
> ユーザーは、フォーム内で変更されたデータを保存する求められます。
    
SAVEOPTS_SAVEIFDIRTY 
  
> 最後の保存以降変更されている場合、フォーム データを保存する必要があります。 ユーザー インターフェイスが表示されていない場合は、フォームを SAVEOPTS_NOSAVE オプションの機能を使用して切り替えることができますオプションで。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォームが閉じられました。
    
E_UNEXPECTED 
  
> **ShutdownForm**の前回の呼び出しで、フォームが既に閉じました。
    
## <a name="remarks"></a>注釈

フォームの閲覧者は、フォームを終了するのには**IMAPIForm::ShutdownForm**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**ShutdownForm**の実装では、次のタスクを実行します。
  
1. 確認しているビューアーが既に呼び出されません**ShutdownForm**とがある場合は E_UNEXPECTED を返します。 ではありませんが、チェックする必要があります。
    
2. 処理が完了するまで、フォームと内部データ構造体のストレージが利用可能なままにするために、フォームの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx)メソッドを呼び出します。 
    
3. フォームのデータに未保存の変更があるかどうかを決定します。 ビューアーの[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)メソッドを呼び出すことによって、 _ulSaveOptions_パラメーターを設定する方法に応じて、保存されていないデータを保存します。 
    
4. フォームのユーザー インターフェイスのウィンドウを破棄します。
    
5. [](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出すことによって、フォームのメッセージとメッセージのサイト オブジェクトを解放します。 
    
6. [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)メソッドを呼び出すことによって登録されているすべての視聴者の保留中のシャット ダウンを通知します。 
    
7. アドバイズ シンク ポインターを**null**に設定して、フォームの登録をキャンセルする[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。
    
8. フォームのプロパティのメモリを解放する[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
    
9. 手順 2 で行われた**AddRef**呼び出しに一致するフォームの**** メソッドを呼び出します。 
    
10. S_OK ��Ԃ��܂��B
    
> [!NOTE]
> これらの操作を完了すると、呼び出される form オブジェクトにのみ有効なメソッドは、 [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)インターフェイスから。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ShutdownForm**制御が戻るとき、エラーを返すかどうかに関係なく、**リ ス**のメソッドを呼び出して、フォームを離します。 **ShutdownForm**によって返されるエラーを無視できます。
  
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

