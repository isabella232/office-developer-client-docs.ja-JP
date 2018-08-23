---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: 夏時間の開始時とでそのタイム ゾーン規則最初が発効した年のタイム ゾーン規則の情報を指定します。
ms.openlocfilehash: 77d56d238d959992bfadd2d8c143391ca6fa4d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799592"
---
# <a name="tzrule"></a><span data-ttu-id="0b596-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="0b596-103">TZRULE</span></span>

<span data-ttu-id="0b596-104">夏時間の開始時とでそのタイム ゾーン規則最初が発効した年のタイム ゾーン規則の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="0b596-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0b596-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0b596-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="0b596-106">Members</span><span class="sxs-lookup"><span data-stu-id="0b596-106">Members</span></span>

<span data-ttu-id="0b596-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="0b596-107">_wFlags_</span></span>
  
> <span data-ttu-id="0b596-108">このメンバーに設定されているフラグは、このタイム ゾーン規則の特定の詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="0b596-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="0b596-109">使用できるフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0b596-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="0b596-110">**TZRULE_FLAG_EFFECTIVE_TZREG** -現在使用すると、ルールを識別します。</span><span class="sxs-lookup"><span data-stu-id="0b596-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="0b596-111">1 つのルールは、有効なルールとしてマークできます。</span><span class="sxs-lookup"><span data-stu-id="0b596-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="0b596-112">他のすべての規則は、比較目的でのみです。</span><span class="sxs-lookup"><span data-stu-id="0b596-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="0b596-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG**などの定期的な会議は、 [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)のルールに一致するルールを識別します。</span><span class="sxs-lookup"><span data-stu-id="0b596-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="0b596-114">これになる場合は、新しいより包括的なプロパティに注意してください、古いバージョンのクライアントで**PidLidTimeZoneStruct**が大幅に変更されているかどうかを検出するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b596-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="0b596-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="0b596-115">_stStart_</span></span>
  
> <span data-ttu-id="0b596-116">世界協定時刻 (UTC) で、タイム ゾーン規則を開始した時刻。</span><span class="sxs-lookup"><span data-stu-id="0b596-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="0b596-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="0b596-117">_TZReg_</span></span>
  
> <span data-ttu-id="0b596-118">タイム ゾーン規則のタイム ゾーン情報。</span><span class="sxs-lookup"><span data-stu-id="0b596-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b596-119">注釈</span><span class="sxs-lookup"><span data-stu-id="0b596-119">Remarks</span></span>

<span data-ttu-id="0b596-120">この構造体は、タイム ゾーン規則が有効になるときを示す追加情報を提供することによって[TZREG](tzreg.md)を補強します。</span><span class="sxs-lookup"><span data-stu-id="0b596-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b596-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b596-121">See also</span></span>

- [<span data-ttu-id="0b596-122">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="0b596-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="0b596-123">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="0b596-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="0b596-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="0b596-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="0b596-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="0b596-125">TZDEFINITION</span></span>](tzdefinition.md)

