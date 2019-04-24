---
title: フォームビューアーの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332894"
---
# <a name="implementing-a-form-viewer"></a><span data-ttu-id="27218-103">フォームビューアーの実装</span><span class="sxs-lookup"><span data-stu-id="27218-103">Implementing a Form Viewer</span></span>

  
  
<span data-ttu-id="27218-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27218-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27218-105">フォームビューアーには、メッセージサイト、ビューアドバイズシンク、ビューコンテキストという3つのオブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="27218-105">A form viewer includes three objects: a message site, a view advise sink, and a view context.</span></span> <span data-ttu-id="27218-106">これらの各オブジェクトを使用すると、フォームサーバーとそのフォームを操作できます。</span><span class="sxs-lookup"><span data-stu-id="27218-106">Each of these objects allows you to interact with a form server and its forms.</span></span>
  
<span data-ttu-id="27218-107">メッセージサイトは、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インターフェイスを実装し、メッセージの移動、保存、削除、新しいメッセージの作成、新しいフォームサーバーの起動などのタスクをフォームサーバーに対して支援するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="27218-107">A message site is an object that implements the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and assists form servers with tasks such as moving, saving, or deleting messages, creating new messages, or launching new form servers.</span></span> <span data-ttu-id="27218-108">メッセージサイトは、さまざまなサービスプロバイダーに関して、クライアントの状態に関する情報を取得するためにフォームによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="27218-108">Message sites are used by forms to get information about your client's status with respect to various service providers.</span></span> <span data-ttu-id="27218-109">たとえば、フォームでメッセージサイトを使用して、現在のメッセージストア、メッセージ、またはフォルダーへのポインターを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="27218-109">For example, a form can use your message site to get a pointer to your current message store, a message, or a folder.</span></span> 
  
<span data-ttu-id="27218-110">**IMAPIMessageSite**インターフェイスには、次の2種類のメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="27218-110">There are two types of methods in the **IMAPIMessageSite** interface:</span></span> 
  
- <span data-ttu-id="27218-111">フォームオブジェクトに情報を提供するメソッド。</span><span class="sxs-lookup"><span data-stu-id="27218-111">Methods that provide information to form objects.</span></span>
    
- <span data-ttu-id="27218-112">メッセージを操作するメソッド。</span><span class="sxs-lookup"><span data-stu-id="27218-112">Methods that manipulate messages.</span></span>
    
<span data-ttu-id="27218-113">フォームオブジェクトに情報を提供するメソッドは、簡単に実装できます。</span><span class="sxs-lookup"><span data-stu-id="27218-113">The methods that provide information to form objects are straightforward to implement.</span></span> <span data-ttu-id="27218-114">[IMAPIMessageSite:: getsitestatus](imapimessagesite-getsitestatus.md)を除くすべての場合に、各メソッドで必要な情報が既に提供されているはずです。</span><span class="sxs-lookup"><span data-stu-id="27218-114">In all cases except [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), you should already have available the information required by each method.</span></span>
  
<span data-ttu-id="27218-115">メッセージを操作するメソッドは、通常のユーザーインターフェイスを使用してトリガーされた場合と同じように動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27218-115">The methods that manipulate messages should act as if they had been triggered through your regular user interface.</span></span> <span data-ttu-id="27218-116">たとえば、form オブジェクトが[IMAPIMessageSite:: newmessage](imapimessagesite-newmessage.md)メソッドを呼び出す場合は、ユーザーが通常のユーザーインターフェイスで新しいカスタムメッセージを作成することを選択した場合と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="27218-116">For example, if a form object calls your [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) method, behave as if the user had chosen to compose a new custom message with your regular user interface.</span></span> <span data-ttu-id="27218-117">通常、この動作を生成するコマンドには、**新規作成**、**オープン**、**返信**、**すべての受信者への返信**、**転送**があります。</span><span class="sxs-lookup"><span data-stu-id="27218-117">Commands which typically generate this behavior are **Compose**, **Open**, **Reply**, **Reply to All Recipients**, and **Forward**.</span></span> 
  
<span data-ttu-id="27218-118">ビューコンテキストは、 [imapiviewcontext: IUnknown](imapiviewcontextiunknown.md)インターフェイスを実装するオブジェクトで、現在のメッセージのコンテキストを備えたフォームサーバーを提供します。これにより、サーバーは、フォルダー内の次または前のメッセージに簡単に切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="27218-118">A view context is an object that implements the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface and provides form servers with a context for the current message, allowing servers to easily switch to the next or previous message in the folder.</span></span> <span data-ttu-id="27218-119">フォームは、情報の共有にビューコンテキストを使用します。</span><span class="sxs-lookup"><span data-stu-id="27218-119">A form uses a view context for sharing information.</span></span> <span data-ttu-id="27218-120">ビューコンテキストオブジェクトを使用すると、フォームは次のことができます。</span><span class="sxs-lookup"><span data-stu-id="27218-120">With a view context object, a form can:</span></span> 
  
- <span data-ttu-id="27218-121">通知のためにクライアントに登録します。</span><span class="sxs-lookup"><span data-stu-id="27218-121">Register with your client for notifications.</span></span>
    
- <span data-ttu-id="27218-122">フォルダー内の次または前のメッセージをアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="27218-122">Activate the next or previous message in the folder.</span></span>
    
- <span data-ttu-id="27218-123">印刷情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="27218-123">Get printing information.</span></span>
    
- <span data-ttu-id="27218-124">クライアントの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="27218-124">Get your client's status.</span></span>
    
- <span data-ttu-id="27218-125">メッセージのテキストバージョンを保存するために使用できるストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="27218-125">Get a stream that can be used to save the text version of a message.</span></span>
    
<span data-ttu-id="27218-126">[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インターフェイスのメソッドと同様に、 **imapiviewcontext**のメソッドは、ビューコンテキストに関連するユーザー操作とクライアント機能に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="27218-126">Similar to the methods in the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface, the methods in **IMAPIViewContext** correlate with user actions and client features that relate to the view context.</span></span> <span data-ttu-id="27218-127">たとえば、ビューコンテキストは、次または前のメッセージをアクティブにし、フォルダーの内容を並べ替え、フォルダーのコンテンツをフィルター処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="27218-127">For example, a view context is involved with activating the next or previous message, sorting the contents of the folder, and filtering the contents of the folder.</span></span> 
  
<span data-ttu-id="27218-128">ユーザーがこれらの機能をアクティブにするためにどのようなメカニズムを提供するかは重要ではありませんが、これらの機能のセマンティックが**imapiviewcontext**インターフェイスのメソッドに適切にマップされていることが重要です。</span><span class="sxs-lookup"><span data-stu-id="27218-128">It is not important what mechanism you provide for users to activate these features, it is only important that the semantics of those features map well to the methods in the **IMAPIViewContext** interface.</span></span> 
  
<span data-ttu-id="27218-129">view アドバイズシンクは、 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インターフェイスを実装し、閲覧者に影響するフォームサーバーからの通知を処理し、共同作業を行うためのヘルプフォームおよびフォームビューアーを処理するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="27218-129">A view advise sink is an object that implements the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and handles notifications from form servers that affect your viewer and help forms and form viewers to work together.</span></span> <span data-ttu-id="27218-130">詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27218-130">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span> 
  

