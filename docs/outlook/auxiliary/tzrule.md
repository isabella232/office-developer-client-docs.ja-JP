---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: 夏時間の開始時期と、そのタイムゾーン規則が最初に有効になる年を示すタイムゾーンルールの情報を指定します。
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328617"
---
# <a name="tzrule"></a><span data-ttu-id="5fc05-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="5fc05-103">TZRULE</span></span>

<span data-ttu-id="5fc05-104">夏時間の開始時期と、そのタイムゾーン規則が最初に有効になる年を示すタイムゾーンルールの情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="5fc05-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5fc05-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5fc05-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="5fc05-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="5fc05-106">Members</span></span>

<span data-ttu-id="5fc05-107">_wflags_</span><span class="sxs-lookup"><span data-stu-id="5fc05-107">_wFlags_</span></span>
  
> <span data-ttu-id="5fc05-108">このメンバーに設定されているフラグは、このタイムゾーンルールの詳細を識別します。</span><span class="sxs-lookup"><span data-stu-id="5fc05-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="5fc05-109">使用可能なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5fc05-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="5fc05-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —現在使用されている必要のあるルールを識別します。</span><span class="sxs-lookup"><span data-stu-id="5fc05-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="5fc05-111">有効なルールとしてマークできるルールは1つだけです。</span><span class="sxs-lookup"><span data-stu-id="5fc05-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="5fc05-112">他のすべてのルールは比較のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="5fc05-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="5fc05-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** : 定期的な会議では、 [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)のルールと一致するルールを識別します。</span><span class="sxs-lookup"><span data-stu-id="5fc05-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="5fc05-114">これは、 **PidLidTimeZoneStruct**が従来のクライアントによって大幅に変更されているかどうかを検出するために使用できます。これは、その他の詳細な完全なプロパティを認識しません。</span><span class="sxs-lookup"><span data-stu-id="5fc05-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="5fc05-115">_ststart_</span><span class="sxs-lookup"><span data-stu-id="5fc05-115">_stStart_</span></span>
  
> <span data-ttu-id="5fc05-116">タイムゾーンルールが開始された協定世界時 (UTC) の時間。</span><span class="sxs-lookup"><span data-stu-id="5fc05-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="5fc05-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="5fc05-117">_TZReg_</span></span>
  
> <span data-ttu-id="5fc05-118">タイムゾーンルールのタイムゾーン情報。</span><span class="sxs-lookup"><span data-stu-id="5fc05-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5fc05-119">解説</span><span class="sxs-lookup"><span data-stu-id="5fc05-119">Remarks</span></span>

<span data-ttu-id="5fc05-120">この構造体は、タイムゾーンルールがいつ有効になるかを示す追加情報を提供することによって、 [TZREG](tzreg.md)を強化します。</span><span class="sxs-lookup"><span data-stu-id="5fc05-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5fc05-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fc05-121">See also</span></span>

- [<span data-ttu-id="5fc05-122">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="5fc05-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="5fc05-123">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="5fc05-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="5fc05-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="5fc05-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="5fc05-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="5fc05-125">TZDEFINITION</span></span>](tzdefinition.md)

