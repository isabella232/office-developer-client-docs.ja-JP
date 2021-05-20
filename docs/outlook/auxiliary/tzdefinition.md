---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: 夏時間のすべての履歴、現在、および将来のタイム ゾーン シフト ルールを含む、タイム ゾーン全体を表します。
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429342"
---
# <a name="tzdefinition"></a><span data-ttu-id="2193a-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="2193a-103">TZDEFINITION</span></span>

<span data-ttu-id="2193a-104">夏時間のすべての履歴、現在、および将来のタイム ゾーン シフト ルールを含む、タイム ゾーン全体を表します。</span><span class="sxs-lookup"><span data-stu-id="2193a-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2193a-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2193a-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="2193a-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="2193a-106">Members</span></span>

<span data-ttu-id="2193a-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="2193a-107">_wFlags_</span></span>
  
> <span data-ttu-id="2193a-108">レジストリ内のタイム ゾーンを表すキー名が有効Windows示します。</span><span class="sxs-lookup"><span data-stu-id="2193a-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="2193a-109">各タイム ゾーンは常にキー名で識別される必要があるから、このメンバーは常に値を持つ必要 **TZDEFINITION_FLAG_VALID_KEYNAME。**</span><span class="sxs-lookup"><span data-stu-id="2193a-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="2193a-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="2193a-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="2193a-111">レジストリ内のこのタイム ゾーンのキー Windowsします。</span><span class="sxs-lookup"><span data-stu-id="2193a-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="2193a-112">この名前はローカライズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2193a-112">This name must not be localized.</span></span> <span data-ttu-id="2193a-113">ソフトウェア開発キット (SDK) ヘッダー MAX_PATH windows.h で定義されている Windowsの最大サイズを持っています。 </span><span class="sxs-lookup"><span data-stu-id="2193a-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="2193a-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="2193a-114">_cRules_</span></span>
  
> <span data-ttu-id="2193a-115">この定義のタイム ゾーン ルールの数。</span><span class="sxs-lookup"><span data-stu-id="2193a-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="2193a-116">ルールの最大数は次 **TZ_MAX_RULES。**</span><span class="sxs-lookup"><span data-stu-id="2193a-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="2193a-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="2193a-117">_rgRules_</span></span>
  
> <span data-ttu-id="2193a-118">シフトが発生する時間を表すルールの配列。</span><span class="sxs-lookup"><span data-stu-id="2193a-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2193a-119">注釈</span><span class="sxs-lookup"><span data-stu-id="2193a-119">Remarks</span></span>

<span data-ttu-id="2193a-120">rgRules には少なくとも  *1 つのルールが必要です*  。</span><span class="sxs-lookup"><span data-stu-id="2193a-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="2193a-121">*rgRules* の最初のルールは、最初のルールの *stStart* に関係なく、2 番目のルールが開始されるまで使用するルールと見なされます。</span><span class="sxs-lookup"><span data-stu-id="2193a-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="2193a-122">ルールは、最も古いルールから最新の順に並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="2193a-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="2193a-123">ルール間に重複は許可されません。そのため、以前のルールは新しいルールの開始時に終了すると見なされます。</span><span class="sxs-lookup"><span data-stu-id="2193a-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2193a-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2193a-124">See also</span></span>

- [<span data-ttu-id="2193a-125">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="2193a-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="2193a-126">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="2193a-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="2193a-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="2193a-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

