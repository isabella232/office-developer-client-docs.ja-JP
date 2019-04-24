---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: 夏時間開始時、標準時への復帰時、およびサマータイムシフトの時間数を定義します。
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307841"
---
# <a name="tzreg"></a><span data-ttu-id="d112d-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="d112d-103">TZREG</span></span>

<span data-ttu-id="d112d-104">夏時間開始時、標準時への復帰時、およびサマータイムシフトの時間数を定義します。</span><span class="sxs-lookup"><span data-stu-id="d112d-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d112d-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d112d-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="d112d-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="d112d-106">Members</span></span>

<span data-ttu-id="d112d-107">_lbias_</span><span class="sxs-lookup"><span data-stu-id="d112d-107">_lBias_</span></span>
  
> <span data-ttu-id="d112d-108">グリニッジ標準時 (GMT) からのオフセット。</span><span class="sxs-lookup"><span data-stu-id="d112d-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="d112d-109">_lstandardbias_</span><span class="sxs-lookup"><span data-stu-id="d112d-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="d112d-110">標準時のバイアスからのオフセット。</span><span class="sxs-lookup"><span data-stu-id="d112d-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="d112d-111">_ldayライトバイアス_</span><span class="sxs-lookup"><span data-stu-id="d112d-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="d112d-112">夏時間時のバイアスからのオフセット。</span><span class="sxs-lookup"><span data-stu-id="d112d-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="d112d-113">_ststandarddate_</span><span class="sxs-lookup"><span data-stu-id="d112d-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="d112d-114">標準時に切り替える時刻。</span><span class="sxs-lookup"><span data-stu-id="d112d-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="d112d-115">_stdaylightdate_</span><span class="sxs-lookup"><span data-stu-id="d112d-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="d112d-116">夏時間への切り替え時間。</span><span class="sxs-lookup"><span data-stu-id="d112d-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d112d-117">解説</span><span class="sxs-lookup"><span data-stu-id="d112d-117">Remarks</span></span>

<span data-ttu-id="d112d-118">この構造体は**TIME_ZONE_INFORMATION**に似ています。</span><span class="sxs-lookup"><span data-stu-id="d112d-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="d112d-119">これは、従来のクライアントが定期的な会議のタイムゾーン情報を格納するために使用する構造です。</span><span class="sxs-lookup"><span data-stu-id="d112d-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d112d-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d112d-120">See also</span></span>

- [<span data-ttu-id="d112d-121">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="d112d-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="d112d-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="d112d-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="d112d-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="d112d-123">TZRULE</span></span>](tzrule.md)

