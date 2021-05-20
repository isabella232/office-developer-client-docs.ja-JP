---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437743"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="d6efe-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="d6efe-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="d6efe-104">このメソッドは、ソーシャル コネクタ 2013 Outlookで廃止されました。</span><span class="sxs-lookup"><span data-stu-id="d6efe-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="d6efe-105">注釈</span><span class="sxs-lookup"><span data-stu-id="d6efe-105">Remarks</span></span>

<span data-ttu-id="d6efe-106">ソーシャル コネクタ 2013 Outlookから、OSC は、アクティビティのオンデマンド同期のみをサポートし、アクティビティのキャッシュまたはハイブリッド同期はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="d6efe-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="d6efe-107">OSC では、機能 XML の **cacheActivities** 設定は無視され、このメソッドは呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="d6efe-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="d6efe-108">動的アクティビティの参照をサポートするには [、ISocialSession2::GetActivitiesEx メソッドを実装](isocialsession2-getactivitiesex.md) します。</span><span class="sxs-lookup"><span data-stu-id="d6efe-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="d6efe-109">**cacheActivities を** false、getActivities、**および dynamicActivitiesLookupEx** を **true** に設定すると、代わりに OSC が **ISocialSession2::GetActivitiesEx** を呼び出すプロンプトが表示されます。  </span><span class="sxs-lookup"><span data-stu-id="d6efe-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="d6efe-110">OSC がフレンドのアクティビティを取得する方法の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="d6efe-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6efe-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="d6efe-111">See also</span></span>

- [<span data-ttu-id="d6efe-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6efe-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

