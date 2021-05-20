---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: このメソッドは、OSC 1.1 では推奨されていません。
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439297"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="fa5cf-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="fa5cf-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="fa5cf-104">このメソッドは、OSC 1.1 では推奨されていません。</span><span class="sxs-lookup"><span data-stu-id="fa5cf-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="fa5cf-105">注釈</span><span class="sxs-lookup"><span data-stu-id="fa5cf-105">Remarks</span></span>

<span data-ttu-id="fa5cf-106">OSC 1.1 から、OSC は **GetActivities を呼び出しなくなりました**。</span><span class="sxs-lookup"><span data-stu-id="fa5cf-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="fa5cf-107">OSC は **、dynamicActivitiesLookup の値を無視します**。</span><span class="sxs-lookup"><span data-stu-id="fa5cf-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="fa5cf-108">動的アクティビティの参照をサポートするには [、ISocialSession2::GetActivitiesEx メソッドを実装](isocialsession2-getactivitiesex.md) します。</span><span class="sxs-lookup"><span data-stu-id="fa5cf-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="fa5cf-109">**cacheActivities を** **false** に設定し **、getActivities および dynamicActivitiesLookupEx** を true に設定すると、代わりに OSC に **ISocialSession2::GetActivitiesEx** を呼び出すプロンプトが表示されます。  </span><span class="sxs-lookup"><span data-stu-id="fa5cf-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa5cf-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="fa5cf-110">See also</span></span>

- [<span data-ttu-id="fa5cf-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa5cf-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

