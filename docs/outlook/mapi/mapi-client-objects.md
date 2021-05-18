---
title: MAPI クライアント オブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412409"
---
# <a name="mapi-client-objects"></a><span data-ttu-id="b1daa-103">MAPI クライアント オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b1daa-103">MAPI client objects</span></span>
  
<span data-ttu-id="b1daa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1daa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1daa-105">標準のメッセージング クライアント アプリケーションは、1 つのオブジェクト (アドバイス シンク) のみを実装します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-105">Standard messaging client applications implement only one object — an advise sink.</span></span> <span data-ttu-id="b1daa-106">通知シンクは [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) インターフェイスから継承され、MAPI およびサービス プロバイダーによってイベント通知に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1daa-106">Advise sinks inherit from the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface and are used by MAPI and service providers for event notification.</span></span> <span data-ttu-id="b1daa-107">一部のクライアントでは、進行状況ダイアログ ボックスの表示をサポートする進行状況オブジェクトも実装します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-107">Some clients also implement progress objects to support the display of progress dialog boxes.</span></span> 
  
<span data-ttu-id="b1daa-108">カスタム フォームをサポートするより複雑なクライアントは [、IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) インターフェイスから継承するメッセージ サイト オブジェクトや [、IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) インターフェイスから継承するビュー コンテキスト オブジェクトなど、別のアアドバイス シンク オブジェクトと他のいくつかのオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-108">More complex clients that support custom forms implement another advise sink object and a few other objects, such as the message site object that inherits from the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and the view context object that inherits from the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface.</span></span> <span data-ttu-id="b1daa-109">追加のアアドバイス シンク オブジェクトは [、IMAPIViewAdviseSink : IUnknown インターフェイスから継承](imapiviewadvisesinkiunknown.md) します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-109">The additional advise sink object inherits from the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface.</span></span> 
  
<span data-ttu-id="b1daa-110">次の表は、標準メッセージング クライアントとカスタム フォームの表示をサポートするクライアントによって実装される MAPI オブジェクトの概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="b1daa-110">The following table summarizes the MAPI objects implemented by standard messaging clients and by clients that support the viewing of custom forms.</span></span>
  
|<span data-ttu-id="b1daa-111">**クライアント オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="b1daa-111">**Client object**</span></span>|<span data-ttu-id="b1daa-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="b1daa-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1daa-113">シンクのアドバイス</span><span class="sxs-lookup"><span data-stu-id="b1daa-113">Advise sink</span></span>  <br/> |<span data-ttu-id="b1daa-114">メッセージ ストア、アドレス帳、またはセッションで発生するイベントのコールバック関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-114">Provides a callback function for events that occur in the message store, address book, or the session.</span></span>  <br/> |
|<span data-ttu-id="b1daa-115">メッセージ サイト</span><span class="sxs-lookup"><span data-stu-id="b1daa-115">Message site</span></span>  <br/> |<span data-ttu-id="b1daa-116">フォーム オブジェクトの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-116">Handles the manipulation of form objects.</span></span>  <br/> |
|<span data-ttu-id="b1daa-117">Progress</span><span class="sxs-lookup"><span data-stu-id="b1daa-117">Progress</span></span>  <br/> |<span data-ttu-id="b1daa-118">操作の進行状況を表示するダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-118">Displays a dialog box to show the progress of an operation.</span></span>  <br/> |
|<span data-ttu-id="b1daa-119">View アアドバイス シンク</span><span class="sxs-lookup"><span data-stu-id="b1daa-119">View advise sink</span></span>  <br/> |<span data-ttu-id="b1daa-120">フォームで発生するイベントのコールバック関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-120">Provides callback functions for events that occur in a form.</span></span>  <br/> |
|<span data-ttu-id="b1daa-121">コンテキストの表示</span><span class="sxs-lookup"><span data-stu-id="b1daa-121">View context</span></span>  <br/> |<span data-ttu-id="b1daa-122">フォームの印刷と保存、およびフォーム間の移動のためのコマンドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b1daa-122">Supports commands for printing and saving forms and for navigating between forms.</span></span>  <br/> |
   
<span data-ttu-id="b1daa-123">次の図は、これらの異なるクライアント オブジェクト、継承元のインターフェイス、およびそれらを使用する MAPI コンポーネントの関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="b1daa-123">The following illustration shows the relationship between these different client objects, the interfaces from which they inherit, and the MAPI components that use them.</span></span> 
  
<span data-ttu-id="b1daa-124">![クライアント オブジェクトと対応するインターフェイス](media/amapi_65.gif "クライアント オブジェクトと対応するインターフェイス")</span><span class="sxs-lookup"><span data-stu-id="b1daa-124">![Client objects and corresponding interfaces](media/amapi_65.gif "Client objects and corresponding interfaces")</span></span>
  
<span data-ttu-id="b1daa-125">クライアントは、実装するオブジェクトよりも多くのオブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-125">Clients use many more objects than they implement.</span></span> <span data-ttu-id="b1daa-126">すべてのクライアントは、セッション オブジェクトを使用して、MAPI が実装するさまざまなサービス プロバイダー オブジェクトとオブジェクトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b1daa-126">All clients use a session object to gain access to a wide variety of service provider objects and objects that MAPI implements.</span></span> <span data-ttu-id="b1daa-127">クライアントは、間接的に、セッション、アドレス帳、MAPI が提供する状態オブジェクト、または特定のサービス プロバイダーが実装するさまざまなオブジェクトを介して直接、サービス プロバイダーと対話します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-127">Clients interact with service providers either indirectly, through the session, the address book, or the status objects that MAPI supplies, or directly through a variety of objects that particular service providers implement.</span></span> <span data-ttu-id="b1daa-128">アドレス帳プロバイダーと直接連絡を取る場合、クライアントはアドレス帳コンテナー、メッセージング ユーザー、配布リストを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-128">To make direct contact with address book providers, clients use address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="b1daa-129">メッセージ ストア プロバイダーに直接アクセスするには、クライアントはメッセージ ストア オブジェクト、フォルダー、メッセージ、添付ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-129">To access a message store provider directly, clients use the message store object, folders, messages, and attachments.</span></span> <span data-ttu-id="b1daa-130">サービス プロバイダーが状態オブジェクトをサポートする場合、クライアントは status オブジェクトを使用してサービス プロバイダーの状態を監視できます。</span><span class="sxs-lookup"><span data-stu-id="b1daa-130">When service providers support a status object, clients can use the status object to monitor the service provider's state.</span></span>
  
<span data-ttu-id="b1daa-131">サービス プロバイダーとメッセージ サービス構成をサポートするクライアントは、MAPI が実装する 3 つのオブジェクト (メッセージ サービス管理オブジェクト、プロファイル管理オブジェクト、プロバイダー管理オブジェクト) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-131">Clients that support service provider and message service configuration use three objects that MAPI implements: the message service administration object, profile administration object, and provider administration object.</span></span> <span data-ttu-id="b1daa-132">カスタム フォームを表示するクライアントは、フォーム ライブラリ プロバイダーまたはフォーム サーバーが実装する複数のフォーム オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1daa-132">Clients that display custom forms use several form objects that a form library provider or a form server implements.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1daa-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="b1daa-133">See also</span></span>

- [<span data-ttu-id="b1daa-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1daa-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md) 
- [<span data-ttu-id="b1daa-135">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1daa-135">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)  
- [<span data-ttu-id="b1daa-136">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1daa-136">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
- [<span data-ttu-id="b1daa-137">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="b1daa-137">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

