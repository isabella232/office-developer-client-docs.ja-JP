---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: このメソッドは、Outlook Social Connector 2013 では廃止されました。
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285965"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="bc12f-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="bc12f-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="bc12f-104">このメソッドは、Outlook Social Connector 2013 では廃止されました。</span><span class="sxs-lookup"><span data-stu-id="bc12f-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="bc12f-105">解説</span><span class="sxs-lookup"><span data-stu-id="bc12f-105">Remarks</span></span>

<span data-ttu-id="bc12f-106">Outlook Social Connector 2013 以降では、アクティビティのオンデマンド同期のみをサポートしており、アクティビティのキャッシュまたはハイブリッド同期はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bc12f-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="bc12f-107">.osc は、機能\*\*\*\* XML の cacheactivities 設定を無視し、このメソッドを呼び出すことがなくなります。</span><span class="sxs-lookup"><span data-stu-id="bc12f-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="bc12f-108">動的アクティビティ検索をサポートするには、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="bc12f-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="bc12f-109">**getactivities**と**dynamicActivitiesLookupEx**を**true**に設定します。この場合、 **ISocialSession2:: GetActivitiesEx**を呼び出すよう、.osc に通知されます。</span><span class="sxs-lookup"><span data-stu-id="bc12f-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="bc12f-110">.osc がフレンドのアクティビティを取得する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc12f-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc12f-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="bc12f-111">See also</span></span>

- [<span data-ttu-id="bc12f-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="bc12f-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

