---
title: フォーム サーバーの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f5f76dd0e17abe53b3666f3f00580cc6af1cdcf0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610378"
---
# <a name="launching-a-form-server"></a>フォーム サーバーの起動

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを表示するために、フォームが永続的な記憶域 (つまり、フォーム ライブラリから) から読み込まれたときに発生する一連の操作は、次のとおりです。
  
1. メッセージング クライアントは、メッセージのメッセージ クラス、メッセージ フラグ、およびメッセージの状態を取得します。 この手順は省略可能です。これらのデータが手順 2 で提供されていない場合、フォーム マネージャーはデータを取得します。
    
2. メッセージング クライアントは、 [ターゲット メッセージを使用して IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) を呼び出します。 
    
3. フォーム マネージャーは、適切なフォーム ライブラリからフォーム サーバーを読み込む。 ターゲット メッセージのフォーム サーバーがインストールされていない場合、フォーム マネージャーはフォームの実行可能ファイルもインストールします。
    
4. フォーム マネージャーは、フォーム オブジェクトの [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) を呼び出して、フォーム オブジェクトの [IMAPIForm : IUnknown](imapiformiunknown.md) および [IPersistMessage : IUnknown](ipersistmessageiunknown.md) インターフェイスを取得します。 
    
5. フォーム マネージャーは、ビューアー オブジェクトからメッセージ サイトとメッセージ インターフェイスを使用して [IPersistMessage::Load](ipersistmessage-load.md) を呼び出します。 
    
6. フォーム オブジェクトは、メッセージング クライアントの [IMAPIMessageSite::GetSiteStatus メソッドに呼び出](imapimessagesite-getsitestatus.md) します。 
    
7. フォーム マネージャーは、メッセージング クライアントからビュー コンテキスト インターフェイスを使用して、フォーム オブジェクトの [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) メソッドを呼び出します。 
    
8. フォーム オブジェクトは、メッセージング クライアントの [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) メソッドを呼び出します。 
    
9. フォーム オブジェクトは、メッセージング クライアントの [IMAPIViewContext::GetViewStatus メソッドを呼び出](imapiviewcontext-getviewstatus.md) します。 
    
10. メッセージング クライアントは、ビューアー オブジェクトとメッセージ サイト オブジェクトからビュー コンテキスト インターフェイスを使用して、フォーム オブジェクトの [IMAPIForm::Advise](imapiform-advise.md) メソッドを呼び出します。 
    
11. メッセージング クライアントは、フォーム オブジェクトの [IMAPIForm::D oVerb メソッドを呼び出](imapiform-doverb.md) します。 
    
12. フォーム オブジェクトは、必要に応じてユーザー インターフェイスを作成し、ユーザーと対話します。
    
## <a name="see-also"></a>関連項目



[フォーム サーバーの操作](form-server-interactions.md)

