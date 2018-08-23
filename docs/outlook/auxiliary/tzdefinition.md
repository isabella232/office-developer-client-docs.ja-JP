---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: 夏時間のすべての過去、現在、および将来のタイム ゾーン シフトの規則を含む全体のタイム ゾーンを表します。
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799604"
---
# <a name="tzdefinition"></a><span data-ttu-id="2cf29-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="2cf29-103">TZDEFINITION</span></span>

<span data-ttu-id="2cf29-104">夏時間のすべての過去、現在、および将来のタイム ゾーン シフトの規則を含む全体のタイム ゾーンを表します。</span><span class="sxs-lookup"><span data-stu-id="2cf29-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2cf29-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2cf29-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="2cf29-106">Members</span><span class="sxs-lookup"><span data-stu-id="2cf29-106">Members</span></span>

<span data-ttu-id="2cf29-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="2cf29-107">_wFlags_</span></span>
  
> <span data-ttu-id="2cf29-108">Windows レジストリ内のタイム ゾーンを表すキー名が有効であることを示します。</span><span class="sxs-lookup"><span data-stu-id="2cf29-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="2cf29-109">各タイム ゾーンは、常に、キーの名前で識別する必要があります、ためこのメンバーは常に値を持つ**TZDEFINITION_FLAG_VALID_KEYNAME**。</span><span class="sxs-lookup"><span data-stu-id="2cf29-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="2cf29-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="2cf29-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="2cf29-111">Windows レジストリには、このタイム ゾーンのキーの名前です。</span><span class="sxs-lookup"><span data-stu-id="2cf29-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="2cf29-112">この名前はローカライズされませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf29-112">This name must not be localized.</span></span> <span data-ttu-id="2cf29-113">**MAX_PATH**、Windows ソフトウェア開発キット (SDK) のヘッダー ファイル windows.h で定義されている最大サイズがあります。</span><span class="sxs-lookup"><span data-stu-id="2cf29-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="2cf29-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="2cf29-114">_cRules_</span></span>
  
> <span data-ttu-id="2cf29-115">この定義のタイム ゾーン規則の数です。</span><span class="sxs-lookup"><span data-stu-id="2cf29-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="2cf29-116">ルールの最大数は、 **TZ_MAX_RULES**です。</span><span class="sxs-lookup"><span data-stu-id="2cf29-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="2cf29-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="2cf29-117">_rgRules_</span></span>
  
> <span data-ttu-id="2cf29-118">シフトが発生する可能性を示す規則の配列。</span><span class="sxs-lookup"><span data-stu-id="2cf29-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2cf29-119">注釈</span><span class="sxs-lookup"><span data-stu-id="2cf29-119">Remarks</span></span>

<span data-ttu-id="2cf29-120">*RgRules*では、少なくとも 1 つのルールをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cf29-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="2cf29-121">*RgRules*の最初のルールは、最初のルールの*stStart*に関係なく、2 番目のルールが開始されるまでに使用するルールを使用すると見なされます。</span><span class="sxs-lookup"><span data-stu-id="2cf29-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="2cf29-122">規則は必要があります古いものから順に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="2cf29-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="2cf29-123">以前の規則が新しいルールを起動したときに終了すると判断したため、ルール間の重複はありません。</span><span class="sxs-lookup"><span data-stu-id="2cf29-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2cf29-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2cf29-124">See also</span></span>

- [<span data-ttu-id="2cf29-125">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="2cf29-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="2cf29-126">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="2cf29-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="2cf29-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="2cf29-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

