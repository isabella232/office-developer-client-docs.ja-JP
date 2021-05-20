---
title: フォーム ビューアーの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435818"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="3f8ac-103">フォーム ビューアーの実装</span><span class="sxs-lookup"><span data-stu-id="3f8ac-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="3f8ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f8ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f8ac-105">フォーム ビューアーには、メッセージ サイト、ビューアアドバイス シンク、ビュー コンテキストの 3 つのオブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="3f8ac-106">これらの各オブジェクトを使用すると、フォーム サーバーとそのフォームを操作できます。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="3f8ac-107">メッセージ サイトは [、IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) インターフェイスを実装し、メッセージの移動、保存、削除、新しいメッセージの作成、新しいフォーム サーバーの起動などのタスクをフォーム サーバーに支援するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="3f8ac-108">メッセージ サイトは、さまざまなサービス プロバイダーに関するクライアントの状態に関する情報を取得するためにフォームによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="3f8ac-109">たとえば、フォームはメッセージ サイトを使用して、現在のメッセージ ストア、メッセージ、またはフォルダーへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="3f8ac-110">IMAPIMessageSite インターフェイスには、次の **2 種類のメソッド** があります。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="3f8ac-111">フォーム オブジェクトに情報を提供するメソッド。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="3f8ac-112">メッセージを操作するメソッド。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="3f8ac-113">フォーム オブジェクトに情報を提供するメソッドは、簡単に実装できます。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="3f8ac-114">[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)を除くすべてのケースで、各メソッドで必要な情報が既に用意されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="3f8ac-115">メッセージを操作するメソッドは、通常のユーザー インターフェイスを介してトリガーされた場合と同様に動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="3f8ac-116">たとえば、フォーム オブジェクトが [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) メソッドを呼び出す場合は、ユーザーが通常のユーザー インターフェイスで新しいカスタム メッセージを作成することを選択した場合と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="3f8ac-117">通常、この動作を生成するコマンドは、Compose、Open、Reply、Reply to All **Recipients、** および Forward です。   </span><span class="sxs-lookup"><span data-stu-id="3f8ac-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="3f8ac-118">ビュー コンテキストは [、IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) インターフェイスを実装し、フォーム サーバーに現在のメッセージのコンテキストを提供するオブジェクトであり、サーバーはフォルダー内の次または前のメッセージに簡単に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="3f8ac-119">フォームは、情報を共有するためにビュー コンテキストを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="3f8ac-120">ビュー コンテキスト オブジェクトを使用すると、フォームで次のコマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="3f8ac-121">通知のためにクライアントに登録します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="3f8ac-122">フォルダー内の次または前のメッセージをアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="3f8ac-123">印刷情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-123">Get printing information.</span></span>
    
- <span data-ttu-id="3f8ac-124">クライアントの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-124">Get your client's status.</span></span>
    
- <span data-ttu-id="3f8ac-125">メッセージのテキスト バージョンを保存するために使用できるストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="3f8ac-126">[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)インターフェイスのメソッドと同様に **、IMAPIViewContext** のメソッドは、ビュー コンテキストに関連するユーザー アクションやクライアント機能と相関します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="3f8ac-127">たとえば、ビュー コンテキストは、次または前のメッセージをアクティブ化し、フォルダーの内容を並べ替え、フォルダーの内容をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="3f8ac-128">ユーザーがこれらの機能をアクティブ化するためのメカニズムは重要ではなく、これらの機能のセマンティクスが **IMAPIViewContext** インターフェイスのメソッドにうまくマップすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="3f8ac-129">ビューアアドバイス シンクは [、IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) インターフェイスを実装し、ビューアーに影響を与えるフォーム サーバーからの通知を処理し、フォームとフォーム ビューアーが一緒に作業するのに役立つオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="3f8ac-130">詳細については、「フォーム通知の [送受信」を参照してください](sending-and-receiving-form-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="3f8ac-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

