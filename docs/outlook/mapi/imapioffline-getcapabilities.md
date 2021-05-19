---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433375"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="9c01e-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="9c01e-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="9c01e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c01e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c01e-105">オフライン オブジェクトでコールバックがサポートされる条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="9c01e-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="9c01e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9c01e-106">Parameters</span></span>

 <span data-ttu-id="9c01e-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="9c01e-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="9c01e-108">[out]次の機能フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9c01e-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="9c01e-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="9c01e-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="9c01e-110">オフライン オブジェクトは、オフライン通知を提供できます。</span><span class="sxs-lookup"><span data-stu-id="9c01e-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="9c01e-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="9c01e-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="9c01e-112">オフライン オブジェクトは、オンライン通知を提供できます。</span><span class="sxs-lookup"><span data-stu-id="9c01e-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c01e-113">注釈</span><span class="sxs-lookup"><span data-stu-id="9c01e-113">Remarks</span></span>

<span data-ttu-id="9c01e-114">**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してオフライン オブジェクトを開いた後、クライアントは [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)でクエリを実行して **IMAPIOffline** インターフェイスへのポインターを取得し **、IMAPIOffline::GetCapabilities** を呼び出して、オブジェクトでサポートされるコールバックを検索できます。</span><span class="sxs-lookup"><span data-stu-id="9c01e-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="9c01e-115">その後、クライアントは **IMAPIOfflineMgr** を使用してコールバックを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9c01e-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="9c01e-116">オフライン オブジェクトのメール サーバーによっては、オンラインに行くコールバックをサポートするオブジェクトは、オフラインに行くコールバックを必ずしもサポートしていない点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="9c01e-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="9c01e-117">また、オフライン オブジェクトはオンライン/オフライン以外の変更のコールバックをサポートする場合があります。オフライン状態 API はオンライン/オフラインの変更のみをサポートし、クライアントはそのような機能のみを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c01e-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c01e-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c01e-118">See also</span></span>



[<span data-ttu-id="9c01e-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="9c01e-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="9c01e-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="9c01e-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="9c01e-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="9c01e-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="9c01e-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="9c01e-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9c01e-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="9c01e-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

