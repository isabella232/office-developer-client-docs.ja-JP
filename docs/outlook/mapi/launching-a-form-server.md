---
title: フォームのサーバーを起動します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c70fd9eb771268db4030cefdf2f27b75ae5963b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801273"
---
# <a name="launching-a-form-server"></a>フォームのサーバーを起動します。

  
  
**適用されます**: Outlook 
  
永続ストレージから、フォームを読み込むときに発生する一連の相互作用の (つまり、フォーム ライブラリから) メッセージを表示するのには、次のようにします。
  
1. メッセージング クライアントは、メッセージのメッセージ クラス、メッセージ フラグ、およびメッセージの状態を取得します。 この手順は省略可能です。これらのデータの一部が手順 2 で指定されていない場合に、フォーム マネージャーを取得します。
    
2. メッセージング クライアントは、移行先のメッセージで、 [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)を呼び出します。 
    
3. フォーム マネージャーは、適切なフォーム ライブラリからフォームのサーバーをロードします。 移行先のメッセージのフォームのサーバーがインストールされていない場合、フォーム マネージャーは、フォームの実行可能ファイルにもをインストールします。
    
4. フォーム マネージャーは、フォームのオブジェクトを取得するフォーム オブジェクトの[IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)を呼び出す[IMAPIForm: IUnknown](imapiformiunknown.md)と[IPersistMessage: IUnknown](ipersistmessageiunknown.md)インタ フェースです。 
    
5. フォーム マネージャー インターフェイスを呼び出す[IPersistMessage::Load](ipersistmessage-load.md)メッセージがサイトとメッセージ ビューアー オブジェクトからです。 
    
6. フォーム オブジェクトは、メッセージング クライアントの[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)メソッドをコールバックします。 
    
7. フォーム マネージャーは、メッセージング クライアントからのビューのコンテキストのインターフェイスを使用して、form オブジェクトの[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)メソッドを呼び出します。 
    
8. フォーム オブジェクトは、メッセージング クライアントの[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドをコールバックします。 
    
9. フォーム オブジェクトは、メッセージング クライアントの[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドをコールバックします。 
    
10. メッセージング クライアントは、ビューアー オブジェクトとメッセージのサイト オブジェクトからのコンテキストのインタ フェースをビューでのフォーム オブジェクトの[IMAPIForm::Advise](imapiform-advise.md)メソッドを呼び出します。 
    
11. メッセージング クライアントでは、form オブジェクトの[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドを呼び出します。 
    
12. フォーム オブジェクトは、必要に応じて、ユーザー インターフェイスを作成し、ユーザーと対話します。
    
## <a name="see-also"></a>関連項目



[フォームのサーバー間のやり取り](form-server-interactions.md)

