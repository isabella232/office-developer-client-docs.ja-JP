---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406893"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="5faad-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="5faad-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="5faad-104">このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。</span><span class="sxs-lookup"><span data-stu-id="5faad-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="5faad-105">注釈</span><span class="sxs-lookup"><span data-stu-id="5faad-105">Remarks</span></span>

<span data-ttu-id="5faad-106">ソーシャル コネクタ 2013 Outlookから、OSC は、アクティビティのオンデマンド同期のみをサポートし、アクティビティのキャッシュまたはハイブリッド同期はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="5faad-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="5faad-107">OSC は、機能 XML の **cacheActivities** 設定を無視し、このメソッドを呼び出しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="5faad-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="5faad-108">動的アクティビティの参照をサポートするには [、ISocialSession2::GetActivitiesEx メソッドを実装](isocialsession2-getactivitiesex.md) します。</span><span class="sxs-lookup"><span data-stu-id="5faad-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="5faad-109">**getActivities および** **dynamicActivitiesLookupEx** を true に設定すると、代わりに OSC に **ISocialSession2::GetActivitiesEx** を呼び出すメッセージが表示されます。 </span><span class="sxs-lookup"><span data-stu-id="5faad-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="5faad-110">OSC がフレンドのアクティビティを取得する方法の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="5faad-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5faad-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="5faad-111">See also</span></span>

- [<span data-ttu-id="5faad-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="5faad-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

