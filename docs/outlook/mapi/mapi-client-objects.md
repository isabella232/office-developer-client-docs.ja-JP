---
title: MAPI クライアントオブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319291"
---
# <a name="mapi-client-objects"></a><span data-ttu-id="50953-103">MAPI クライアントオブジェクト</span><span class="sxs-lookup"><span data-stu-id="50953-103">MAPI client objects</span></span>
  
<span data-ttu-id="50953-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50953-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50953-105">標準のメッセージングクライアントアプリケーションは、1つのオブジェクト (アドバイズシンク) のみを実装します。</span><span class="sxs-lookup"><span data-stu-id="50953-105">Standard messaging client applications implement only one object — an advise sink.</span></span> <span data-ttu-id="50953-106">アドバイズシンクは[IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インターフェイスから継承し、イベント通知用に MAPI およびサービスプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="50953-106">Advise sinks inherit from the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface and are used by MAPI and service providers for event notification.</span></span> <span data-ttu-id="50953-107">一部のクライアントは、進行状況のダイアログボックスの表示をサポートするために、進行状況オブジェクトも実装します。</span><span class="sxs-lookup"><span data-stu-id="50953-107">Some clients also implement progress objects to support the display of progress dialog boxes.</span></span> 
  
<span data-ttu-id="50953-108">カスタムフォームをサポートするより複雑なクライアントでは、別のアドバイズシンクオブジェクトと、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インターフェイスから継承するメッセージサイトオブジェクト、およびその他のいくつかのオブジェクトを実装します。[imapiviewcontext: IUnknown](imapiviewcontextiunknown.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="50953-108">More complex clients that support custom forms implement another advise sink object and a few other objects, such as the message site object that inherits from the [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) interface and the view context object that inherits from the [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) interface.</span></span> <span data-ttu-id="50953-109">追加のアドバイズシンクオブジェクトは、 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インターフェイスから継承します。</span><span class="sxs-lookup"><span data-stu-id="50953-109">The additional advise sink object inherits from the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface.</span></span> 
  
<span data-ttu-id="50953-110">次の表に、標準のメッセージングクライアントと、カスタムフォームの表示をサポートするクライアントによって実装される MAPI オブジェクトの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="50953-110">The following table summarizes the MAPI objects implemented by standard messaging clients and by clients that support the viewing of custom forms.</span></span>
  
|<span data-ttu-id="50953-111">**クライアントオブジェクト**</span><span class="sxs-lookup"><span data-stu-id="50953-111">**Client object**</span></span>|<span data-ttu-id="50953-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="50953-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50953-113">アドバイズシンク</span><span class="sxs-lookup"><span data-stu-id="50953-113">Advise sink</span></span>  <br/> |<span data-ttu-id="50953-114">メッセージストア、アドレス帳、またはセッションで発生するイベントのコールバック関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="50953-114">Provides a callback function for events that occur in the message store, address book, or the session.</span></span>  <br/> |
|<span data-ttu-id="50953-115">メッセージサイト</span><span class="sxs-lookup"><span data-stu-id="50953-115">Message site</span></span>  <br/> |<span data-ttu-id="50953-116">form オブジェクトの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="50953-116">Handles the manipulation of form objects.</span></span>  <br/> |
|<span data-ttu-id="50953-117">Progress</span><span class="sxs-lookup"><span data-stu-id="50953-117">Progress</span></span>  <br/> |<span data-ttu-id="50953-118">操作の進行状況を示すダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="50953-118">Displays a dialog box to show the progress of an operation.</span></span>  <br/> |
|<span data-ttu-id="50953-119">アドバイズシンクの表示</span><span class="sxs-lookup"><span data-stu-id="50953-119">View advise sink</span></span>  <br/> |<span data-ttu-id="50953-120">フォームで発生するイベントのコールバック関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="50953-120">Provides callback functions for events that occur in a form.</span></span>  <br/> |
|<span data-ttu-id="50953-121">ビューのコンテキスト</span><span class="sxs-lookup"><span data-stu-id="50953-121">View context</span></span>  <br/> |<span data-ttu-id="50953-122">フォームの印刷および保存、およびフォーム間の移動に使用するコマンドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="50953-122">Supports commands for printing and saving forms and for navigating between forms.</span></span>  <br/> |
   
<span data-ttu-id="50953-123">次の図は、これらの異なるクライアントオブジェクト、継承元のインターフェイス、およびそれらを使用する MAPI コンポーネントの関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="50953-123">The following illustration shows the relationship between these different client objects, the interfaces from which they inherit, and the MAPI components that use them.</span></span> 
  
<span data-ttu-id="50953-124">![クライアントオブジェクトと対応するインターフェイス](media/amapi_65.gif "クライアントオブジェクトと対応するインターフェイス")</span><span class="sxs-lookup"><span data-stu-id="50953-124">![Client objects and corresponding interfaces](media/amapi_65.gif "Client objects and corresponding interfaces")</span></span>
  
<span data-ttu-id="50953-125">クライアントは、実装されているよりも多くのオブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="50953-125">Clients use many more objects than they implement.</span></span> <span data-ttu-id="50953-126">すべてのクライアントは session オブジェクトを使用して、MAPI が実装するさまざまなサービスプロバイダーオブジェクトおよびオブジェクトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="50953-126">All clients use a session object to gain access to a wide variety of service provider objects and objects that MAPI implements.</span></span> <span data-ttu-id="50953-127">クライアントは、サービスプロバイダーを間接的に、セッション、アドレス帳、または MAPI が提供する status オブジェクトを通じて、または特定のサービスプロバイダーが実装しているさまざまなオブジェクトによって対話します。</span><span class="sxs-lookup"><span data-stu-id="50953-127">Clients interact with service providers either indirectly, through the session, the address book, or the status objects that MAPI supplies, or directly through a variety of objects that particular service providers implement.</span></span> <span data-ttu-id="50953-128">アドレス帳プロバイダーと直接連絡先を作成するために、クライアントはアドレス帳コンテナー、メッセージングユーザー、および配布リストを使用します。</span><span class="sxs-lookup"><span data-stu-id="50953-128">To make direct contact with address book providers, clients use address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="50953-129">メッセージストアプロバイダーに直接アクセスする場合、クライアントはメッセージストアオブジェクト、フォルダー、メッセージ、および添付ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="50953-129">To access a message store provider directly, clients use the message store object, folders, messages, and attachments.</span></span> <span data-ttu-id="50953-130">サービスプロバイダーが status オブジェクトをサポートしている場合、クライアントは status オブジェクトを使用して、サービスプロバイダーの状態を監視できます。</span><span class="sxs-lookup"><span data-stu-id="50953-130">When service providers support a status object, clients can use the status object to monitor the service provider's state.</span></span>
  
<span data-ttu-id="50953-131">サービスプロバイダーとメッセージサービスの構成をサポートするクライアントは、MAPI が実装する3つのオブジェクトを使用します。メッセージサービスの管理オブジェクト、プロファイル管理オブジェクト、およびプロバイダー管理オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="50953-131">Clients that support service provider and message service configuration use three objects that MAPI implements: the message service administration object, profile administration object, and provider administration object.</span></span> <span data-ttu-id="50953-132">ユーザー設定フォームを表示するクライアントは、フォームライブラリプロバイダーまたはフォームサーバーが実装する複数のフォームオブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="50953-132">Clients that display custom forms use several form objects that a form library provider or a form server implements.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50953-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="50953-133">See also</span></span>

- [<span data-ttu-id="50953-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50953-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md) 
- [<span data-ttu-id="50953-135">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50953-135">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)  
- [<span data-ttu-id="50953-136">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50953-136">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
- [<span data-ttu-id="50953-137">MAPI のオブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="50953-137">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

