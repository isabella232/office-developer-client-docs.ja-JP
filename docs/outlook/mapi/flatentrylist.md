---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336898"
---
# <a name="flatentrylist"></a><span data-ttu-id="14b11-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="14b11-103">FLATENTRYLIST</span></span>

<span data-ttu-id="14b11-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14b11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14b11-105">[FLATENTRY](flatentry.md)構造体の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="14b11-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14b11-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="14b11-106">Header file:</span></span>  <br/> |<span data-ttu-id="14b11-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="14b11-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="14b11-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="14b11-108">Related macros:</span></span>  <br/> |<span data-ttu-id="14b11-109">[CbFLATENTRYLIST](cbflatentrylist.md)、 [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="14b11-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="14b11-110">Members</span><span class="sxs-lookup"><span data-stu-id="14b11-110">Members</span></span>

<span data-ttu-id="14b11-111">**centries**</span><span class="sxs-lookup"><span data-stu-id="14b11-111">**cEntries**</span></span>
  
> <span data-ttu-id="14b11-112">**abentries**メンバーによって記述された、配列内の**FLATENTRY**構造体の数。</span><span class="sxs-lookup"><span data-stu-id="14b11-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="14b11-113">**cbentries**</span><span class="sxs-lookup"><span data-stu-id="14b11-113">**cbEntries**</span></span>
  
> <span data-ttu-id="14b11-114">**abentries**で記述された配列内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="14b11-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="14b11-115">**abentries**</span><span class="sxs-lookup"><span data-stu-id="14b11-115">**abEntries**</span></span>
  
> <span data-ttu-id="14b11-116">1つまたは複数の**FLATENTRY**構造を含むバイト配列。エンドツーエンドで配置されています。</span><span class="sxs-lookup"><span data-stu-id="14b11-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="14b11-117">解説</span><span class="sxs-lookup"><span data-stu-id="14b11-117">Remarks</span></span>

<span data-ttu-id="14b11-118">**abentries**配列では、各**FLATENTRY**構造は、自然に配置された境界に沿って配置されます。</span><span class="sxs-lookup"><span data-stu-id="14b11-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="14b11-119">2つの**FLATENTRY**構造体間で自然な配置が行われるように、パディングとして追加のバイトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="14b11-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="14b11-120">**abentries**メンバーのオフセットは8であるため、配列内の最初の**FLATENTRY**構造体は常に正確に調整されます。</span><span class="sxs-lookup"><span data-stu-id="14b11-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="14b11-121">次の構造体のオフセットを計算するには、最初のエントリのサイズを、次の4つの倍数まで切り上げて使用します。</span><span class="sxs-lookup"><span data-stu-id="14b11-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="14b11-122">[CbFLATENTRY](cbflatentry.md)マクロを使用して、 **FLATENTRY**構造体のサイズを計算します。</span><span class="sxs-lookup"><span data-stu-id="14b11-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="14b11-123">たとえば、2番目の**FLATENTRY**構造体は、最初のエントリのオフセットと、次の4バイトに丸められた最初のエントリの長さで構成されるオフセットから始まります。</span><span class="sxs-lookup"><span data-stu-id="14b11-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="14b11-124">最初のエントリの長さは、 **cb**メンバーの長さに**abentry**メンバーの長さを加えたものです。</span><span class="sxs-lookup"><span data-stu-id="14b11-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="14b11-125">次のコードサンプルは、 **FLATENTRYLIST**構造体でオフセットを計算する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="14b11-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="14b11-126">_lpFlatEntry_はリスト内の最初の構造体へのポインターであると仮定します。</span><span class="sxs-lookup"><span data-stu-id="14b11-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="14b11-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="14b11-127">See also</span></span>

- [<span data-ttu-id="14b11-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="14b11-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="14b11-129">PidTagReplyRecipientEntries 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="14b11-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="14b11-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="14b11-130">MAPI Structures</span></span>](mapi-structures.md)

