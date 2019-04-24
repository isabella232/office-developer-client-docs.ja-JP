---
title: imapiofflinegetcapabilities
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321316"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="8b5be-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="8b5be-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="8b5be-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b5be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b5be-105">オフラインオブジェクトでサポートされているコールバックの条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="8b5be-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="8b5be-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b5be-106">Parameters</span></span>

 <span data-ttu-id="8b5be-107">_アウト (アウト)_</span><span class="sxs-lookup"><span data-stu-id="8b5be-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="8b5be-108">読み上げ次の機能フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8b5be-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="8b5be-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="8b5be-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="8b5be-110">オフラインオブジェクトがオフライン通知を提供できる。</span><span class="sxs-lookup"><span data-stu-id="8b5be-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="8b5be-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="8b5be-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="8b5be-112">オフラインオブジェクトは、オンライン通知を提供できます。</span><span class="sxs-lookup"><span data-stu-id="8b5be-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b5be-113">解説</span><span class="sxs-lookup"><span data-stu-id="8b5be-113">Remarks</span></span>

<span data-ttu-id="8b5be-114">**[hropenofflineobj](hropenofflineobj.md)** を使用してオフラインオブジェクトを開くときに、クライアントは[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)上でクエリを実行して**imapioffline**インターフェイスへのポインターを取得し、 **imapioffline:: getcapabilities**を呼び出して、サポートされているコールバックを検索できます。オブジェクトによって。</span><span class="sxs-lookup"><span data-stu-id="8b5be-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="8b5be-115">クライアントは、 **IMAPIOfflineMgr**を使用してコールバックをセットアップすることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="8b5be-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="8b5be-116">オフラインオブジェクトのメールサーバーによっては、オンラインに移行するためのコールバックをサポートするオブジェクトが、必ずしもオフラインへのコールバックをサポートするわけではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8b5be-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="8b5be-117">また、オフラインオブジェクトはオンライン/オフライン以外の変更に対するコールバックをサポートしていますが、オフライン状態 API はオンライン/オフライン変更のみをサポートしており、クライアントはそのような機能だけをチェックする必要があることにも注意してください。</span><span class="sxs-lookup"><span data-stu-id="8b5be-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b5be-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="8b5be-118">See also</span></span>



[<span data-ttu-id="8b5be-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="8b5be-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="8b5be-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="8b5be-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="8b5be-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="8b5be-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="8b5be-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="8b5be-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8b5be-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="8b5be-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

