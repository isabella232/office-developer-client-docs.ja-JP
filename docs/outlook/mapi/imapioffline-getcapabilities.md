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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 699e77479e0d09e7549c0d2741d5ba54ecc8ce33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572033"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="04855-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="04855-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="04855-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04855-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04855-105">コールバックは、オフラインのオブジェクトによってサポートされている条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="04855-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="04855-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04855-106">Parameters</span></span>

 <span data-ttu-id="04855-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="04855-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="04855-108">[out]以下の機能フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="04855-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="04855-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="04855-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="04855-110">オフライン オブジェクトはオフラインの通知を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="04855-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="04855-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="04855-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="04855-112">オフラインのオブジェクトでは、オンラインの通知を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="04855-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04855-113">注釈</span><span class="sxs-lookup"><span data-stu-id="04855-113">Remarks</span></span>

<span data-ttu-id="04855-114">**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してオフラインのオブジェクトを開くときにクライアントは、 **IMAPIOffline**インターフェイスへのポインターを取得し、サポートされているコールバックを確認するのには、 **IMAPIOffline::GetCapabilities**を呼び出すには、 [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)に問い合わせることができます。オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="04855-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="04855-115">**IMAPIOfflineMgr**を使用してコールバックを設定するクライアントを選択できます。</span><span class="sxs-lookup"><span data-stu-id="04855-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="04855-116">オフライン オブジェクトのメール サーバー、オンラインのコールバックをサポートするオブジェクトは必ずしもサポート コールバック オフラインになるため注意してください。</span><span class="sxs-lookup"><span data-stu-id="04855-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="04855-117">なお、いる間以外のオンラインまたはオフラインの変更のオフライン オブジェクトがコールバックをサポート可能性があります、オフライン状態の API は、オンラインとオフラインの変更のみをサポートしているクライアントは、このような機能だけを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04855-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04855-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="04855-118">See also</span></span>



[<span data-ttu-id="04855-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="04855-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="04855-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="04855-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="04855-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="04855-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="04855-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="04855-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="04855-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="04855-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

