---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 26, 2021
ms.openlocfilehash: 67a0fffdd0ab6d4989c12568f4d89808ba5adc7a
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062040"
---
# <a name="imapiwaitresult--iunknown"></a><span data-ttu-id="eb52c-103">IMAPIWaitResult : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb52c-103">IMAPIWaitResult : IUnknown</span></span>
  
<span data-ttu-id="eb52c-104">**適用対象 :** Outlook 2013 |Outlook 2016 |Outlook 2019</span><span class="sxs-lookup"><span data-stu-id="eb52c-104">**Applies to**: Outlook 2013 | Outlook 2016 | Outlook 2019</span></span>

<span data-ttu-id="eb52c-105">このインターフェイスは、IMAPIInitMonitor のコンシューマーが待機の発生場所を制御するために使用します。</span><span class="sxs-lookup"><span data-stu-id="eb52c-105">This interface is used by consumers of IMAPIInitMonitor to control where the wait happens.</span></span> <span data-ttu-id="eb52c-106">これにより、オブジェクトを 1 つのスレッドに作成し、別のスレッドに移動して実際の待機を実行できます。</span><span class="sxs-lookup"><span data-stu-id="eb52c-106">It allows them create the object on one thread and move it another thread to perform the actual wait.</span></span>

## <a name="vtable-order"></a><span data-ttu-id="eb52c-107">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="eb52c-107">Vtable order</span></span>

| <span data-ttu-id="eb52c-108">function</span><span class="sxs-lookup"><span data-stu-id="eb52c-108">function</span></span> | <span data-ttu-id="eb52c-109">説明</span><span class="sxs-lookup"><span data-stu-id="eb52c-109">description</span></span> |
|:-----|:-----|
|[<span data-ttu-id="eb52c-110">HRESULT IMAPIWaitResult::End()</span><span class="sxs-lookup"><span data-stu-id="eb52c-110">HRESULT IMAPIWaitResult::End()</span></span>](imapiwaitresult-end.md)|<span data-ttu-id="eb52c-111">呼び出されたスレッドでブロック待機を開始するために呼び出されます *。IMAPIInitMonitor::BeginWait* と呼ばれるスレッドとは異なっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb52c-111">Called to initiate the blocking wait on the thread where it is called, which does not need to be the same thread that called *IMAPIInitMonitor::BeginWait*.</span></span>|

| <span data-ttu-id="eb52c-112">クイック 情報</span><span class="sxs-lookup"><span data-stu-id="eb52c-112">quick info</span></span> | <span data-ttu-id="eb52c-113">result</span><span class="sxs-lookup"><span data-stu-id="eb52c-113">result</span></span> |
|:-----|:-----|
|<span data-ttu-id="eb52c-114">継承元:</span><span class="sxs-lookup"><span data-stu-id="eb52c-114">Inherits from:</span></span>  <br/> |<span data-ttu-id="eb52c-115">IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb52c-115">IUnknown</span></span>  <br/> |
|<span data-ttu-id="eb52c-116">実装元:</span><span class="sxs-lookup"><span data-stu-id="eb52c-116">Implemented by:</span></span>  <br/> |  <span data-ttu-id="eb52c-117">OLMAPI32.DLL</span><span class="sxs-lookup"><span data-stu-id="eb52c-117">OLMAPI32.DLL</span></span><br/> |
|<span data-ttu-id="eb52c-118">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="eb52c-118">Called by:</span></span>  <br/> |<span data-ttu-id="eb52c-119">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="eb52c-119">Client applications</span></span>  <br/> |
|<span data-ttu-id="eb52c-120">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="eb52c-120">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eb52c-121">IID_IMAPIWaitResult</span><span class="sxs-lookup"><span data-stu-id="eb52c-121">IID_IMAPIWaitResult</span></span>  <br/> |

## <a name="see-also"></a><span data-ttu-id="eb52c-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb52c-122">See also</span></span>

[<span data-ttu-id="eb52c-123">IMAPIInitMonitor</span><span class="sxs-lookup"><span data-stu-id="eb52c-123">IMAPIInitMonitor</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="eb52c-124">IMAPIInitMonitor::BeginWait</span><span class="sxs-lookup"><span data-stu-id="eb52c-124">IMAPIInitMonitor::BeginWait</span></span>](imapiinitmonitor-beginwait.md)

[<span data-ttu-id="eb52c-125">IMAPIInitMonitor : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb52c-125">IMAPIInitMonitor : IUnknown</span></span>](imapiinitmonitoriunknown.md)

[<span data-ttu-id="eb52c-126">CreateMAPIInitializationMonitor</span><span class="sxs-lookup"><span data-stu-id="eb52c-126">CreateMAPIInitializationMonitor</span></span>](createmapiinitializationmonitor.md)
