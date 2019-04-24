---
title: i社会 al個人 getアクティビティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: このメソッドは、Outlook Social Connector 2013 では廃止されました。
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286165"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="e9085-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="e9085-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="e9085-104">このメソッドは、Outlook Social Connector 2013 では廃止されました。</span><span class="sxs-lookup"><span data-stu-id="e9085-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="e9085-105">解説</span><span class="sxs-lookup"><span data-stu-id="e9085-105">Remarks</span></span>

<span data-ttu-id="e9085-106">Outlook Social Connector 2013 以降では、アクティビティのオンデマンド同期のみをサポートしており、アクティビティのキャッシュまたはハイブリッド同期はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e9085-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="e9085-107">.osc は、機能 XML の**cacheactivities**設定を無視し、このメソッドを呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="e9085-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="e9085-108">動的アクティビティ検索をサポートするには、 [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="e9085-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="e9085-109">**cacheactivities**を**false**、 **getactivities** 、 **dynamicActivitiesLookupEx**を**true**に設定し、 **ISocialSession2:: GetActivitiesEx**を呼び出すように、.osc に通知されます。</span><span class="sxs-lookup"><span data-stu-id="e9085-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="e9085-110">.osc がフレンドのアクティビティを取得する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9085-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9085-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9085-111">See also</span></span>

- [<span data-ttu-id="e9085-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9085-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

