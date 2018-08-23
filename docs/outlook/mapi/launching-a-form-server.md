---
title: フォーム サーバーの起動
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
# <a name="launching-a-form-server"></a><span data-ttu-id="7cee6-103">フォーム サーバーの起動</span><span class="sxs-lookup"><span data-stu-id="7cee6-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="7cee6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cee6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cee6-105">永続ストレージから、フォームを読み込むときに発生する一連の相互作用の (つまり、フォーム ライブラリから) メッセージを表示するのには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="7cee6-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="7cee6-106">メッセージング クライアントは、メッセージのメッセージ クラス、メッセージ フラグ、およびメッセージの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="7cee6-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="7cee6-107">この手順は省略可能です。これらのデータの一部が手順 2 で指定されていない場合に、フォーム マネージャーを取得します。</span><span class="sxs-lookup"><span data-stu-id="7cee6-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="7cee6-108">メッセージング クライアントは、移行先のメッセージで、 [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7cee6-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="7cee6-109">フォーム マネージャーは、適切なフォーム ライブラリからフォームのサーバーをロードします。</span><span class="sxs-lookup"><span data-stu-id="7cee6-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="7cee6-110">移行先のメッセージのフォームのサーバーがインストールされていない場合、フォーム マネージャーは、フォームの実行可能ファイルにもをインストールします。</span><span class="sxs-lookup"><span data-stu-id="7cee6-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="7cee6-111">フォーム マネージャーは、フォームのオブジェクトを取得するフォーム オブジェクトの[IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)を呼び出す[IMAPIForm: IUnknown](imapiformiunknown.md)と[IPersistMessage: IUnknown](ipersistmessageiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="7cee6-111">The form manager calls [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="7cee6-112">フォーム マネージャー インターフェイスを呼び出す[IPersistMessage::Load](ipersistmessage-load.md)メッセージがサイトとメッセージ ビューアー オブジェクトからです。</span><span class="sxs-lookup"><span data-stu-id="7cee6-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="7cee6-113">フォーム オブジェクトは、メッセージング クライアントの[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)メソッドをコールバックします。</span><span class="sxs-lookup"><span data-stu-id="7cee6-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="7cee6-114">フォーム マネージャーは、メッセージング クライアントからのビューのコンテキストのインターフェイスを使用して、form オブジェクトの[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7cee6-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="7cee6-115">フォーム オブジェクトは、メッセージング クライアントの[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドをコールバックします。</span><span class="sxs-lookup"><span data-stu-id="7cee6-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="7cee6-116">フォーム オブジェクトは、メッセージング クライアントの[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)メソッドをコールバックします。</span><span class="sxs-lookup"><span data-stu-id="7cee6-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="7cee6-117">メッセージング クライアントは、ビューアー オブジェクトとメッセージのサイト オブジェクトからのコンテキストのインタ フェースをビューでのフォーム オブジェクトの[IMAPIForm::Advise](imapiform-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7cee6-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="7cee6-118">メッセージング クライアントでは、form オブジェクトの[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7cee6-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="7cee6-119">フォーム オブジェクトは、必要に応じて、ユーザー インターフェイスを作成し、ユーザーと対話します。</span><span class="sxs-lookup"><span data-stu-id="7cee6-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7cee6-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="7cee6-120">See also</span></span>



[<span data-ttu-id="7cee6-121">フォーム サーバーの相互作用</span><span class="sxs-lookup"><span data-stu-id="7cee6-121">Form Server Interactions</span></span>](form-server-interactions.md)

