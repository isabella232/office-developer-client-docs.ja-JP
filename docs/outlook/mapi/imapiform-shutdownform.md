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

 _ulSaveOptions_
  
> [in]フォームを閉じる前に、フォーム内のデータを保存する方法またはかどうかを制御する値。 次のいずれかのフラグを設定できます。
    
SAVEOPTS_NOSAVE 
  
> フォーム データを保存する必要があります。
    
SAVEOPTS_PROMPTSAVE 
  
> ユーザーは、フォームに変更されたデータを保存するように求めるメッセージが表示されます。
    
SAVEOPTS_SAVEIFDIRTY 
  
> フォーム データは、前回の保存以降に変更された場合に保存する必要があります。 ユーザー インターフェイスが表示されない場合は、必要に応じてフォームを [ユーザー インターフェイス] オプションの機能を使用SAVEOPTS_NOSAVEできます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームが閉じられました。
    
E_UNEXPECTED 
  
> このフォームは、ShutdownForm の事前呼び出しによって既 **に閉じられました**。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIForm::ShutdownForm** メソッドを呼び出してフォームを閉じます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

ShutdownForm の実装で次のタスク **を実行します**。
  
1. ビューアーが **ShutdownForm** をまだ呼び出していないか確認し、存在する場合E_UNEXPECTEDを返します。 これはありそうもないが、確認する必要があります。
    
2. フォームの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) メソッドを呼び出して、フォームのストレージと内部データ構造を処理が完了するまで使用できます。 
    
3. フォームのデータに保存されていない変更が含されているかどうかを判断します。 ビューアーの [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)メソッドを呼び出して _、ulSaveOptions_ パラメーターの設定方法に従って、保存されていないデータを保存します。 
    
4. フォームのユーザー インターフェイス ウィンドウを破棄します。
    
5. フォームのメッセージおよびメッセージ サイト オブジェクトを [解放するには、IUnknown::Release メソッドを呼び](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) 出します。 
    
6. [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)メソッドを呼び出して、保留中のシャットダウンを登録しているすべてのビューアーに通知します。 
    
7. [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出して、アドバイス シンク ポインターを null に設定して、通知のためにフォームの登録をキャンセル **します**。
    
8. [MAPIFreeBuffer 関数を呼](mapifreebuffer.md)び出して、フォームのプロパティのメモリを解放します。 
    
9. 手順 2 で行った **AddRef** 呼び出しと一致する、フォームの **IUnknown::Release** メソッドを呼び出します。 
    
10. S_OK ��Ԃ��܂��B
    
> [!NOTE]
> これらのアクションが完了すると、呼び出される可能性があるフォーム オブジェクトの有効なメソッドは [、IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) インターフェイスからのメソッドのみです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**ShutdownForm が** 返された場合、エラーが返されるかどうかに関係なく **、IUnknown::Release** メソッドを呼び出してフォームを解放します。 ShutdownForm によって返されるエラーは無視しても **問題ない**。
  
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

