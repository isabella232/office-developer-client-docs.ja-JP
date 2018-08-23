---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: OSC 1.1 に、このメソッドは廃止されました。
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804361"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="21b0e-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="21b0e-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="21b0e-104">OSC 1.1 に、このメソッドは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="21b0e-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="21b0e-105">注釈</span><span class="sxs-lookup"><span data-stu-id="21b0e-105">Remarks</span></span>

<span data-ttu-id="21b0e-106">OSC 1.1 以降では、OSC は不要になった、 **GetActivities**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="21b0e-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="21b0e-107">OSC では、 **dynamicActivitiesLookup**の値を無視します。</span><span class="sxs-lookup"><span data-stu-id="21b0e-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="21b0e-108">参照の動的な活動をサポートするには、 [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="21b0e-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="21b0e-109">**False**、 **getActivities**と**true を指定**する代わりに**ISocialSession2::GetActivitiesEx**を呼び出す OSC を求めるメッセージが表示、 **dynamicActivitiesLookupEx** 、 **cacheActivities**を設定します。</span><span class="sxs-lookup"><span data-stu-id="21b0e-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="21b0e-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="21b0e-110">See also</span></span>

- [<span data-ttu-id="21b0e-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="21b0e-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

