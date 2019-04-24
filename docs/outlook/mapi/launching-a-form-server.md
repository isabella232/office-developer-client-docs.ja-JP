---
title: フォームサーバーの起動
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
# <a name="launching-a-form-server"></a><span data-ttu-id="5d412-103">フォームサーバーの起動</span><span class="sxs-lookup"><span data-stu-id="5d412-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="5d412-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d412-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d412-105">フォームが永続的なストレージ (フォームライブラリから) から読み込まれてメッセージを表示するときに発生する一連の対話は、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5d412-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="5d412-106">メッセージングクライアントは、メッセージのメッセージクラス、メッセージフラグ、およびメッセージの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="5d412-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="5d412-107">この手順は省略できます。このようなデータが手順2で提供されていない場合は、フォームマネージャーが取得します。</span><span class="sxs-lookup"><span data-stu-id="5d412-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="5d412-108">メッセージングクライアントは、ターゲットメッセージと共に[imapiformmgr:: loadform](imapiformmgr-loadform.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5d412-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="5d412-109">フォームマネージャーは、フォームサーバーを適切なフォームライブラリから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="5d412-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="5d412-110">ターゲットメッセージのフォームサーバーがインストールされていない場合、フォームマネージャーはフォームの実行可能ファイルもインストールします。</span><span class="sxs-lookup"><span data-stu-id="5d412-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="5d412-111">フォームマネージャーは form オブジェクトの[iunknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)を呼び出して、form オブジェクトの[imapiform: iunknown](imapiformiunknown.md)インターフェイスと[IPersistMessage: iunknown](ipersistmessageiunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="5d412-111">The form manager calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="5d412-112">フォームマネージャーは、 [IPersistMessage:: Load](ipersistmessage-load.md)というメッセージサイトとメッセージインターフェイスを viewer オブジェクトから呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5d412-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="5d412-113">form オブジェクトは、メッセージングクライアントの[IMAPIMessageSite:: getsitestatus](imapimessagesite-getsitestatus.md)メソッドに呼び出しを戻します。</span><span class="sxs-lookup"><span data-stu-id="5d412-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="5d412-114">フォームマネージャーは、フォームオブジェクトの[imapiform:: setviewcontext](imapiform-setviewcontext.md)メソッドによって、メッセージングクライアントからビューコンテキストインターフェイスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5d412-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="5d412-115">form オブジェクトは、メッセージングクライアントの[imapiviewcontext:: SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドに呼び出しを戻します。</span><span class="sxs-lookup"><span data-stu-id="5d412-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="5d412-116">form オブジェクトは、メッセージングクライアントの[imapiviewcontext:: getviewstatus](imapiviewcontext-getviewstatus.md)メソッドに呼び出しを戻します。</span><span class="sxs-lookup"><span data-stu-id="5d412-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="5d412-117">メッセージングクライアントは、フォームオブジェクトの[imapiform:: Advise](imapiform-advise.md)メソッドを viewer オブジェクトおよびメッセージサイトオブジェクトからのビューコンテキストインターフェイスで呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5d412-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="5d412-118">メッセージングクライアントは、form オブジェクトの[imapiform を呼び出します。:D overb](imapiform-doverb.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="5d412-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="5d412-119">form オブジェクトは、必要に応じて、そのユーザーインターフェイスを作成し、ユーザーと対話します。</span><span class="sxs-lookup"><span data-stu-id="5d412-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d412-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d412-120">See also</span></span>



[<span data-ttu-id="5d412-121">フォームサーバーの相互作用</span><span class="sxs-lookup"><span data-stu-id="5d412-121">Form Server Interactions</span></span>](form-server-interactions.md)

