---
title: フォーム サーバーの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270050"
---
# <a name="launching-a-form-server"></a><span data-ttu-id="c59ae-103">フォーム サーバーの起動</span><span class="sxs-lookup"><span data-stu-id="c59ae-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="c59ae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c59ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c59ae-105">メッセージを表示するために、フォームが永続的な記憶域 (つまり、フォーム ライブラリから) から読み込まれたときに発生する一連の操作は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c59ae-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="c59ae-106">メッセージング クライアントは、メッセージのメッセージ クラス、メッセージ フラグ、およびメッセージの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="c59ae-107">この手順は省略可能です。これらのデータが手順 2 で提供されていない場合、フォーム マネージャーはデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="c59ae-108">メッセージング クライアントは、 [ターゲット メッセージを使用して IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="c59ae-109">フォーム マネージャーは、適切なフォーム ライブラリからフォーム サーバーを読み込む。</span><span class="sxs-lookup"><span data-stu-id="c59ae-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="c59ae-110">ターゲット メッセージのフォーム サーバーがインストールされていない場合、フォーム マネージャーはフォームの実行可能ファイルもインストールします。</span><span class="sxs-lookup"><span data-stu-id="c59ae-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="c59ae-111">フォーム マネージャーは、フォーム オブジェクトの [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) を呼び出して、フォーム オブジェクトの [IMAPIForm : IUnknown](imapiformiunknown.md) および [IPersistMessage : IUnknown](ipersistmessageiunknown.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-111">The form manager calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="c59ae-112">フォーム マネージャーは、ビューアー オブジェクトからメッセージ サイトとメッセージ インターフェイスを使用して [IPersistMessage::Load](ipersistmessage-load.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="c59ae-113">フォーム オブジェクトは、メッセージング クライアントの [IMAPIMessageSite::GetSiteStatus メソッドに呼び出](imapimessagesite-getsitestatus.md) します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="c59ae-114">フォーム マネージャーは、メッセージング クライアントからビュー コンテキスト インターフェイスを使用して、フォーム オブジェクトの [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="c59ae-115">フォーム オブジェクトは、メッセージング クライアントの [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="c59ae-116">フォーム オブジェクトは、メッセージング クライアントの [IMAPIViewContext::GetViewStatus メソッドを呼び出](imapiviewcontext-getviewstatus.md) します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="c59ae-117">メッセージング クライアントは、ビューアー オブジェクトとメッセージ サイト オブジェクトからビュー コンテキスト インターフェイスを使用して、フォーム オブジェクトの [IMAPIForm::Advise](imapiform-advise.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="c59ae-118">メッセージング クライアントは、フォーム オブジェクトの [IMAPIForm::D oVerb メソッドを呼び出](imapiform-doverb.md) します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="c59ae-119">フォーム オブジェクトは、必要に応じてユーザー インターフェイスを作成し、ユーザーと対話します。</span><span class="sxs-lookup"><span data-stu-id="c59ae-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c59ae-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="c59ae-120">See also</span></span>



[<span data-ttu-id="c59ae-121">フォーム サーバーの操作</span><span class="sxs-lookup"><span data-stu-id="c59ae-121">Form Server Interactions</span></span>](form-server-interactions.md)

