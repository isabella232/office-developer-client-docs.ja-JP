---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Outlook ソーシャル コネクタ 2013 では、このメソッドは廃止されました。
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804378"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="4f6e8-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="4f6e8-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="4f6e8-104">Outlook ソーシャル コネクタ 2013 では、このメソッドは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="4f6e8-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="4f6e8-105">備考</span><span class="sxs-lookup"><span data-stu-id="4f6e8-105">Remarks</span></span>

<span data-ttu-id="4f6e8-106">Outlook ソーシャル コネクタ 2013、OSC の活動のみ、オンデマンド同期をサポートしている、キャッシュされていない、または活動のハイブリッド同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="4f6e8-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="4f6e8-107">OSC では、XML の機能の**cacheActivities**の設定を無視し、不要になったこのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4f6e8-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="4f6e8-108">参照の動的な活動をサポートするには、 [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="4f6e8-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="4f6e8-109">**GetActivities**と**dynamicActivitiesLookupEx**を**true を指定**する代わりに**ISocialSession2::GetActivitiesEx**を呼び出す OSC を求めるメッセージが表示に設定します。</span><span class="sxs-lookup"><span data-stu-id="4f6e8-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="4f6e8-110">OSC が友人の活動を取得する方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f6e8-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f6e8-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f6e8-111">See also</span></span>

- [<span data-ttu-id="4f6e8-112">ISocialProfile: ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="4f6e8-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

