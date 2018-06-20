---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: 時刻が夏時間の開始時、標準時間へのリターンが発生すると、および夏時間のシフトは、時間数を定義します。
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799594"
---
# <a name="tzreg"></a><span data-ttu-id="2dd79-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="2dd79-103">TZREG</span></span>

<span data-ttu-id="2dd79-104">時刻が夏時間の開始時、標準時間へのリターンが発生すると、および夏時間のシフトは、時間数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2dd79-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2dd79-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2dd79-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="2dd79-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="2dd79-106">Members</span></span>

<span data-ttu-id="2dd79-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="2dd79-107">_lBias_</span></span>
  
> <span data-ttu-id="2dd79-108">グリニッジ標準時 (GMT) からのオフセット。</span><span class="sxs-lookup"><span data-stu-id="2dd79-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="2dd79-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="2dd79-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="2dd79-110">標準時間の間のバイアスからのオフセット。</span><span class="sxs-lookup"><span data-stu-id="2dd79-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="2dd79-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="2dd79-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="2dd79-112">サマータイム期間中のバイアスからのオフセット。</span><span class="sxs-lookup"><span data-stu-id="2dd79-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="2dd79-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="2dd79-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="2dd79-114">(標準時) に切り替えるには時間です。</span><span class="sxs-lookup"><span data-stu-id="2dd79-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="2dd79-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="2dd79-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="2dd79-116">夏時間への切り替えにかかる時間です。</span><span class="sxs-lookup"><span data-stu-id="2dd79-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2dd79-117">備考</span><span class="sxs-lookup"><span data-stu-id="2dd79-117">Remarks</span></span>

<span data-ttu-id="2dd79-118">この構造体は、 **TIME_ZONE_INFORMATION**に似ています。</span><span class="sxs-lookup"><span data-stu-id="2dd79-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="2dd79-119">これは、定期的なミーティングのタイム ゾーン情報を保存するのにはレガシ クライアントで使用する構造体です。</span><span class="sxs-lookup"><span data-stu-id="2dd79-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2dd79-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="2dd79-120">See also</span></span>

- [<span data-ttu-id="2dd79-121">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="2dd79-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="2dd79-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="2dd79-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="2dd79-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="2dd79-123">TZRULE</span></span>](tzrule.md)

