---
title: MAPI クライアント オブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fb37c15e6544798a956e865e6c8c6d62bee44d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801342"
---
# <a name="mapi-client-objects"></a><span data-ttu-id="2b8a2-103">MAPI クライアント オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2b8a2-103">MAPI client objects</span></span>
  
<span data-ttu-id="2b8a2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2b8a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2b8a2-105">メッセージング クライアント アプリケーションの標準的な実装の 1 つのオブジェクト、アドバイズ シンクします。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-105">Standard messaging client applications implement only one object — an advise sink.</span></span> <span data-ttu-id="2b8a2-106">シンクの継承からのアドバイス、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インタ フェースおよび MAPI によってし、イベント通知のためのプロバイダーのサービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-106">Advise sinks inherit from the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface and are used by MAPI and service providers for event notification.</span></span> <span data-ttu-id="2b8a2-107">一部のクライアントでは、進行状況ダイアログ ボックスの表示をサポートするために進行中のオブジェクトも実装します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-107">Some clients also implement progress objects to support the display of progress dialog boxes.</span></span> 
  
<span data-ttu-id="2b8a2-108">複雑なクライアントのサポートのユーザー設定フォームが別のアドバイスを実装するオブジェクトとメッセージ サイト オブジェクトから継承するなど、他のいくつかのオブジェクトのシンク、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インタ フェースとビュー コンテキスト オブジェクトから継承する、[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-108">More complex clients that support custom forms implement another advise sink object and a few other objects, such as the message site object that inherits from the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and the view context object that inherits from the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface.</span></span> <span data-ttu-id="2b8a2-109">追加のアドバイズ シンク オブジェクトの継承、 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-109">The additional advise sink object inherits from the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface.</span></span> 
  
<span data-ttu-id="2b8a2-110">次の表は、標準メッセージング クライアントとユーザー設定フォームの表示をサポートするクライアントによって実装される MAPI オブジェクトをまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-110">The following table summarizes the MAPI objects implemented by standard messaging clients and by clients that support the viewing of custom forms.</span></span>
  
|<span data-ttu-id="2b8a2-111">**クライアント オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="2b8a2-111">**Client object**</span></span>|<span data-ttu-id="2b8a2-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="2b8a2-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2b8a2-113">アドバイズ シンク</span><span class="sxs-lookup"><span data-stu-id="2b8a2-113">Advise sink</span></span>  <br/> |<span data-ttu-id="2b8a2-114">メッセージ ・ ストア、アドレス帳、またはセッションで発生するイベントのコールバック関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-114">Provides a callback function for events that occur in the message store, address book, or the session.</span></span>  <br/> |
|<span data-ttu-id="2b8a2-115">メッセージ サイト</span><span class="sxs-lookup"><span data-stu-id="2b8a2-115">Message site</span></span>  <br/> |<span data-ttu-id="2b8a2-116">フォーム オブジェクトの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-116">Handles the manipulation of form objects.</span></span>  <br/> |
|<span data-ttu-id="2b8a2-117">Progress</span><span class="sxs-lookup"><span data-stu-id="2b8a2-117">Progress</span></span>  <br/> |<span data-ttu-id="2b8a2-118">操作の進行状況を表示するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-118">Displays a dialog box to show the progress of an operation.</span></span>  <br/> |
|<span data-ttu-id="2b8a2-119">ビューのアドバイズ シンク</span><span class="sxs-lookup"><span data-stu-id="2b8a2-119">View advise sink</span></span>  <br/> |<span data-ttu-id="2b8a2-120">フォームで発生するイベントのコールバック関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-120">Provides callback functions for events that occur in a form.</span></span>  <br/> |
|<span data-ttu-id="2b8a2-121">ビュー コンテキスト</span><span class="sxs-lookup"><span data-stu-id="2b8a2-121">View context</span></span>  <br/> |<span data-ttu-id="2b8a2-122">印刷、フォームを保存し、フォーム間を移動するには、コマンドをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-122">Supports commands for printing and saving forms and for navigating between forms.</span></span>  <br/> |
   
<span data-ttu-id="2b8a2-123">次の図は、これらのさまざまなクライアント オブジェクト、継承、インターフェイスおよびそれらを使用する MAPI コンポーネント間の関係を示します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-123">The following illustration shows the relationship between these different client objects, the interfaces from which they inherit, and the MAPI components that use them.</span></span> 
  
<span data-ttu-id="2b8a2-124">![[クライアント オブジェクトおよび対応するインターフェイス](media/amapi_65.gif "[クライアント オブジェクトおよび対応するインターフェイス")</span><span class="sxs-lookup"><span data-stu-id="2b8a2-124">![Client objects and corresponding interfaces](media/amapi_65.gif "Client objects and corresponding interfaces")</span></span>
  
<span data-ttu-id="2b8a2-125">クライアントは、実装するよりも多くのより多くのオブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-125">Clients use many more objects than they implement.</span></span> <span data-ttu-id="2b8a2-126">すべてのクライアントは、さまざまなサービス ・ プロバイダーのオブジェクトや MAPI を実装するオブジェクトへのアクセスを得るために、セッション オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-126">All clients use a session object to gain access to a wide variety of service provider objects and objects that MAPI implements.</span></span> <span data-ttu-id="2b8a2-127">クライアントは、セッション、アドレス帳、または MAPI が提供する状態オブジェクトを介して間接的に、または特定のサービス プロバイダーを実装するオブジェクトのさまざまなを使用して直接のいずれかのサービス プロバイダーと対話します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-127">Clients interact with service providers either indirectly, through the session, the address book, or the status objects that MAPI supplies, or directly through a variety of objects that particular service providers implement.</span></span> <span data-ttu-id="2b8a2-128">アドレス帳プロバイダーへの直接連絡をするためは、クライアントは、ユーザー、および配布リストのメッセージ、アドレス帳コンテナーで使用します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-128">To make direct contact with address book providers, clients use address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="2b8a2-129">メッセージ ストア プロバイダーにアクセスするのには、直接クライアントを使用してメッセージ ストアのオブジェクト、フォルダー、メッセージ、および添付ファイルです。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-129">To access a message store provider directly, clients use the message store object, folders, messages, and attachments.</span></span> <span data-ttu-id="2b8a2-130">サービス プロバイダーは、状態オブジェクトをサポート、すると、クライアントはサービス プロバイダーの状態を監視するのに状態オブジェクトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-130">When service providers support a status object, clients can use the status object to monitor the service provider's state.</span></span>
  
<span data-ttu-id="2b8a2-131">サービス プロバイダーとサービスのメッセージの構成をサポートするクライアントが MAPI を実装する 3 つのオブジェクトを使用して: メッセージ サービスの管理オブジェクト、管理、および、プロバイダーの管理オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-131">Clients that support service provider and message service configuration use three objects that MAPI implements: the message service administration object, profile administration object, and provider administration object.</span></span> <span data-ttu-id="2b8a2-132">カスタム フォームを表示するクライアントは、フォーム ライブラリのプロバイダーまたはフォーム サーバーを実装するいくつかのフォーム オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="2b8a2-132">Clients that display custom forms use several form objects that a form library provider or a form server implements.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b8a2-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b8a2-133">See also</span></span>

- [<span data-ttu-id="2b8a2-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b8a2-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md) 
- [<span data-ttu-id="2b8a2-135">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b8a2-135">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)  
- [<span data-ttu-id="2b8a2-136">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b8a2-136">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
- [<span data-ttu-id="2b8a2-137">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="2b8a2-137">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

