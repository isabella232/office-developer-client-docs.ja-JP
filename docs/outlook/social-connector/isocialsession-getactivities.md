---
title: i社会 alsessiongetアクティビティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: このメソッドは、.osc 1.1 では廃止されました。
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285456"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="7880b-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="7880b-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="7880b-104">このメソッドは、.osc 1.1 では廃止されました。</span><span class="sxs-lookup"><span data-stu-id="7880b-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="7880b-105">解説</span><span class="sxs-lookup"><span data-stu-id="7880b-105">Remarks</span></span>

<span data-ttu-id="7880b-106">.osc 1.1 から、.osc は**getactivities**を呼び出すことがなくなりました。</span><span class="sxs-lookup"><span data-stu-id="7880b-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="7880b-107">.osc では、 **dynamicActivitiesLookup**の値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="7880b-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="7880b-108">動的アクティビティ検索をサポートするには、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="7880b-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="7880b-109">**cacheactivities**を**false**に設定し、 **getactivities**と**dynamicActivitiesLookupEx**を**true**として設定します。これにより、 **ISocialSession2:: GetActivitiesEx**を呼び出すように、.osc に通知されます。</span><span class="sxs-lookup"><span data-stu-id="7880b-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7880b-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="7880b-110">See also</span></span>

- [<span data-ttu-id="7880b-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7880b-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

