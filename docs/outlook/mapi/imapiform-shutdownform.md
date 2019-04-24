---
title: imapiformshutdownform
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329478"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームを閉じます。
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>パラメーター

 _ulsaveoptions_
  
> 順番フォームを閉じる前に、フォーム内のデータを保存するかどうかを制御する値を指定します。 次のいずれかのフラグを設定できます。
    
SAVEOPTS_NOSAVE 
  
> フォームデータは保存しないようにします。
    
SAVEOPTS_PROMPTSAVE 
  
> ユーザーは、変更されたデータをフォームに保存するかどうかを確認するメッセージを表示する必要があります。
    
SAVEOPTS_SAVEIFDIRTY 
  
> 前回の保存以降に変更されている場合は、フォームデータを保存する必要があります。 ユーザーインターフェイスが表示されていない場合は、必要に応じて、SAVEOPTS_NOSAVE オプションの機能を使用してフォームを切り替えることができます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが閉じられました。
    
E_UNEXPECTED 
  
> このフォームは、以前に**shutdownform**を呼び出したときに既に閉じられています。
    
## <a name="remarks"></a>解説

フォームビューアーは、 **imapiform:: shutdownform**メソッドを呼び出してフォームを閉じます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**shutdownform**の実装で、次のタスクを実行します。
  
1. viewer が**shutdownform**を呼び出していないことを確認し、E_UNEXPECTED がある場合はそれを返します。 このことはほとんどありませんが、確認する必要があります。
    
2. フォームの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)メソッドを呼び出して、フォームおよび内部データ構造のストレージを処理が完了するまで引き続き使用できるようにします。 
    
3. フォームのデータに保存されていない変更があるかどうかを確認します。 [IMAPIMessageSite:: SaveMessage](imapimessagesite-savemessage.md)メソッドを呼び出すことにより、 _ulsaveoptions_パラメーターの設定方法に従って未保存のデータを保存します。 
    
4. フォームのユーザーインターフェイスウィンドウを破棄します。
    
5. [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドを呼び出して、フォームのメッセージおよびメッセージサイトオブジェクトを解放します。 
    
6. [IMAPIViewAdviseSink:: onshutdown](imapiviewadvisesink-onshutdown.md)メソッドを呼び出して、保留中のシャットダウンのすべての登録済みビューアーに通知します。 
    
7. [imapiviewcontext:: SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出して、アドバイズシンクポインターを**null**に設定することにより、フォームの通知の登録を取り消します。
    
8. [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、フォームのプロパティのメモリを解放します。 
    
9. 手順2で作成した**AddRef**呼び出しに一致するように、フォームの**IUnknown:: Release**メソッドを呼び出します。 
    
10. S_OK ��Ԃ��܂��B
    
> [!NOTE]
> これらの操作が完了した後、呼び出される可能性のある form オブジェクトの有効なメソッドは、 [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスからのものだけです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

エラーが返されるかどうかに関係なく、 **shutdownform**から制御が戻ると、 **IUnknown:: release**メソッドを呼び出してフォームを解放します。 **shutdownform**によって返されるエラーは無視しても問題ありません。
  
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

