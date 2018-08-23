---
title: フォーム ビューアーの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ad0da261b3059ca83f2d547c25a508ec9337aa72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584745"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="9fcdf-103">フォーム ビューアーの実装</span><span class="sxs-lookup"><span data-stu-id="9fcdf-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="9fcdf-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fcdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fcdf-105">フォーム ビューアーには、3 つのオブジェクトが含まれています: メッセージのサイトでは、ビューのアドバイズ シンク、およびビューのコンテキスト。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="9fcdf-106">これらの各オブジェクトにより、フォームのサーバーと、フォームと対話することができます。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="9fcdf-107">メッセージ サイトを実装するオブジェクトでは、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インタ フェースし、フォームのサーバーの移動、保存、またはメッセージを削除する、新しいメッセージを作成するフォームの新しいサーバーを起動するなどのタスクを支援します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="9fcdf-108">メッセージのサイトは、さまざまなサービス ・ プロバイダーに対して、クライアントのステータスに関する情報を取得するのには、フォームによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="9fcdf-109">たとえば、フォームは、現在のメッセージ ストア、メッセージ、またはフォルダーへのポインターを取得するのには、メッセージのサイトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="9fcdf-110">**IMAPIMessageSite**インターフェイスのメソッドの 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="9fcdf-111">フォーム オブジェクトに情報を提供する方法があります。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="9fcdf-112">メッセージを操作する方法があります。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="9fcdf-113">フォーム オブジェクトに情報を提供する方法は、実装するために簡単です。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="9fcdf-114">[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)を除くすべての場合、既に利用可能な各メソッドに必要な情報です。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="9fcdf-115">メッセージを操作するメソッドの動作は、通常のユーザー インターフェイスを介してトリガーされるされていた場合は、必要があります。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="9fcdf-116">たとえば、フォーム オブジェクトの[IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md)メソッドを呼び出すと場合、は、正規のユーザー インターフェイスと新しいカスタム メッセージを作成するのには、ユーザーが選択した場合と同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="9fcdf-117">通常この現象を生成するコマンドは、**作成**、**開く**、**返信**、**すべての受信者への返信**、および**転送**されます。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="9fcdf-118">ビュー コンテキストを実装するオブジェクトとは、 [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)インターフェイスし、サーバー フォルダー内の次または前のメッセージを簡単に切り替えるには、現在のメッセージのコンテキストとフォームのサーバーを提供します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="9fcdf-119">フォームは、情報を共有するためのビュー コンテキストを使用します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="9fcdf-120">ビュー コンテキスト オブジェクトは、フォームは次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="9fcdf-121">お客様の通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="9fcdf-122">フォルダー内の次または前のメッセージを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="9fcdf-123">印刷の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-123">Get printing information.</span></span>
    
- <span data-ttu-id="9fcdf-124">クライアントのステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-124">Get your client's status.</span></span>
    
- <span data-ttu-id="9fcdf-125">メッセージのテキスト バージョンを保存するのに使用できるストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="9fcdf-126">内のメソッドのような[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インタ フェースでは、 **IMAPIViewContext**内のメソッドと相互に関連のユーザーのアクションとビューのコンテキストに関連するクライアントの機能です。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="9fcdf-127">たとえば、次または前のメッセージをアクティブにする、フォルダーの内容を並べ替え、およびフォルダーの内容をフィルター処理でビューのコンテキストが関係します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="9fcdf-128">重要ではありませんどのようなメカニズムをユーザーに提供するこれらの機能を有効にするのにはこれらの機能の意味が**IMAPIViewContext**インターフェイスのメソッドにマップされる重要な。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="9fcdf-129">ビューのアドバイズ シンクを実装するオブジェクトでは、 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)ビューアー、およびヘルプのフォーム、フォームの閲覧者は、共同作業に影響を与えるフォームのサーバーからのインタ フェースとハンドルの通知します。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="9fcdf-130">詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9fcdf-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

