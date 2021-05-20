---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 26, 2021
ms.openlocfilehash: dd17d50b04755d9d9c2a10a9b02cd821faf1f7ec
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062047"
---
# <a name="imapiinitmonitor--iunknown"></a><span data-ttu-id="5ca87-103">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ca87-103">IMAPIInitMonitor : IUnknown</span></span>

<span data-ttu-id="5ca87-104">**適用対象 :** Outlook 2013 |Outlook 2016 |Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="5ca87-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="5ca87-105">MAPI を使用するアプリケーションが、初期化が完了した時間を知りたい場合があります。</span><span class="sxs-lookup"><span data-stu-id="5ca87-105">There are times when an application which consumes MAPI might want to know when the initialization is completed.</span></span> <span data-ttu-id="5ca87-106">たとえば、MAPI を初期化できる複数のスレッドがある場合や、MAPI の初期化に応答してアプリケーションが何らかの処理を実行する必要がありますが、MAPI スタックを常にスピンアップする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5ca87-106">For example, it has multiple threads which could initialize MAPI, or in response to MAPI being initialized the application would like perform some work, but does not want to always spin up the MAPI stack.</span></span> <span data-ttu-id="5ca87-107">初期化モニターは [、CreateMAPIInitializationMonitor オブジェクトを介してこの機能を提供](createmapiinitializationmonitor.md) します。</span><span class="sxs-lookup"><span data-stu-id="5ca87-107">The initialization monitor provides this functionality through a [CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md) object.</span></span>

| <span data-ttu-id="5ca87-108">クイック 情報</span><span class="sxs-lookup"><span data-stu-id="5ca87-108">quick info</span></span> | <span data-ttu-id="5ca87-109">result</span><span class="sxs-lookup"><span data-stu-id="5ca87-109">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="5ca87-110">継承元:</span><span class="sxs-lookup"><span data-stu-id="5ca87-110">Inherits from:</span></span>  <br/> |<span data-ttu-id="5ca87-111">IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ca87-111">IUnknown</span></span>  <br/> |
|<span data-ttu-id="5ca87-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="5ca87-112">Implemented by:</span></span>  <br/> | <span data-ttu-id="5ca87-113">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="5ca87-113">OLMAPI32.DLL</span></span> <br/> |
|<span data-ttu-id="5ca87-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5ca87-114">Called by:</span></span>  <br/> |<span data-ttu-id="5ca87-115">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5ca87-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="5ca87-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="5ca87-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5ca87-117">IID_IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="5ca87-117">IID_IMAPIInitMonitor</span></span>  <br/> |

## <a name="vtable-order"></a><span data-ttu-id="5ca87-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="5ca87-118">Vtable order</span></span>

| <span data-ttu-id="5ca87-119">function</span><span class="sxs-lookup"><span data-stu-id="5ca87-119">function</span></span> | <span data-ttu-id="5ca87-120">説明</span><span class="sxs-lookup"><span data-stu-id="5ca87-120">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="5ca87-121">IMAPIInitMonitor::IsInitialized</span><span class="sxs-lookup"><span data-stu-id="5ca87-121">IMAPIInitMonitor::IsInitialized</span></span>](imapiinitmonitor-isinitialized.md) <br/> |<span data-ttu-id="5ca87-122">MAPI の初期化の現在の状態を返します。</span><span class="sxs-lookup"><span data-stu-id="5ca87-122">Returns the current state of MAPI initialization.</span></span>  <br/> |
|[<span data-ttu-id="5ca87-123">IMAPIInitMonitor::Wait</span><span class="sxs-lookup"><span data-stu-id="5ca87-123">IMAPIInitMonitor::Wait</span></span>](imapiinitmonitor-wait.md) <br/> |<span data-ttu-id="5ca87-124">このスレッドで BLOCKING 呼び出しを開始します。指定したミリ秒数が経過するか、MAPI が初期化された場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="5ca87-124">Initiates a BLOCKING call on this thread, which will return either when the specified number of milliseconds have elapsed or MAPI has been initialized.</span></span>  <span data-ttu-id="5ca87-125">INFINITE は、無限の待機に使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ca87-125">INFINITE can be used to for an infinite wait.</span></span>  <br/> |
|[<span data-ttu-id="5ca87-126">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="5ca87-126">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md) <br/> |<span data-ttu-id="5ca87-127">MAPI の初期化または指定した経過時間 (ミリ秒単位) の待機を開始します。</span><span class="sxs-lookup"><span data-stu-id="5ca87-127">Start a wait for MAPI initialization or the specified number of milliseconds to elapse.</span></span> <span data-ttu-id="5ca87-128">これにより、IMAPIWaitResult インターフェイスが返され、待機を開始するために "End" が呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ca87-128">This return an IMAPIWaitResult interface which should have “End” called in order begin the wait.</span></span>  <span data-ttu-id="5ca87-129">これにより、呼び出し元は、待機中にブロックされるスレッドを制御できます。</span><span class="sxs-lookup"><span data-stu-id="5ca87-129">This allows the caller to control which thread is blocked while we are waiting.</span></span> <br/> |
