---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: 夏時間のすべての過去、現在、および今後のタイムゾーンシフトルールを含むタイムゾーン全体を表します。
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328295"
---
# <a name="tzdefinition"></a><span data-ttu-id="3ede4-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="3ede4-103">TZDEFINITION</span></span>

<span data-ttu-id="3ede4-104">夏時間のすべての過去、現在、および今後のタイムゾーンシフトルールを含むタイムゾーン全体を表します。</span><span class="sxs-lookup"><span data-stu-id="3ede4-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3ede4-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3ede4-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="3ede4-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="3ede4-106">Members</span></span>

<span data-ttu-id="3ede4-107">_wflags_</span><span class="sxs-lookup"><span data-stu-id="3ede4-107">_wFlags_</span></span>
  
> <span data-ttu-id="3ede4-108">Windows レジストリのタイムゾーンを表すキー名が有効であることを示します。</span><span class="sxs-lookup"><span data-stu-id="3ede4-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="3ede4-109">各タイムゾーンは常にキー名によって識別される必要があるため、このメンバーの値は常に**TZDEFINITION_FLAG_VALID_KEYNAME**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ede4-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="3ede4-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="3ede4-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="3ede4-111">Windows レジストリ内のこのタイムゾーンのキーの名前。</span><span class="sxs-lookup"><span data-stu-id="3ede4-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="3ede4-112">この名前はローカライズしないでください。</span><span class="sxs-lookup"><span data-stu-id="3ede4-112">This name must not be localized.</span></span> <span data-ttu-id="3ede4-113">これは、windows Software Development Kit (SDK) ヘッダーファイル windows で定義されている**MAX_PATH**の最大サイズを持ちます。</span><span class="sxs-lookup"><span data-stu-id="3ede4-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="3ede4-114">_crules しくみ_</span><span class="sxs-lookup"><span data-stu-id="3ede4-114">_cRules_</span></span>
  
> <span data-ttu-id="3ede4-115">この定義のタイムゾーンルールの数。</span><span class="sxs-lookup"><span data-stu-id="3ede4-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="3ede4-116">ルールの最大数は**TZ_MAX_RULES**です。</span><span class="sxs-lookup"><span data-stu-id="3ede4-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="3ede4-117">_rgrules_</span><span class="sxs-lookup"><span data-stu-id="3ede4-117">_rgRules_</span></span>
  
> <span data-ttu-id="3ede4-118">シフトが発生するタイミングを記述するルールの配列です。</span><span class="sxs-lookup"><span data-stu-id="3ede4-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ede4-119">解説</span><span class="sxs-lookup"><span data-stu-id="3ede4-119">Remarks</span></span>

<span data-ttu-id="3ede4-120">*rgrules* 、少なくとも1つのルールが必要です。</span><span class="sxs-lookup"><span data-stu-id="3ede4-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="3ede4-121">[ *rgrules*の最初のルールは、最初のルールの*ststart*に関係なく、2番目のルールが開始されるまで使用するルールと見なされます。</span><span class="sxs-lookup"><span data-stu-id="3ede4-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="3ede4-122">ルールは、最も古いものから [最新] に順に並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ede4-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="3ede4-123">ルール間に重複が許可されていないため、新しいルールが開始される前のルールが終了したと見なされます。</span><span class="sxs-lookup"><span data-stu-id="3ede4-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ede4-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ede4-124">See also</span></span>

- [<span data-ttu-id="3ede4-125">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="3ede4-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="3ede4-126">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="3ede4-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="3ede4-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="3ede4-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

