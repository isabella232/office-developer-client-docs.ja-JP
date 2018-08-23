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
ms.openlocfilehash: 371d0305f8f00e66704bae03f93857c7275b6a10
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589820"
---
# <a name="flatentrylist"></a><span data-ttu-id="5e904-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="5e904-103">FLATENTRYLIST</span></span>

<span data-ttu-id="5e904-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e904-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e904-105">[FLATENTRY](flatentry.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e904-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e904-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5e904-106">Header file:</span></span>  <br/> |<span data-ttu-id="5e904-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e904-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5e904-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="5e904-108">Related macros:</span></span>  <br/> |<span data-ttu-id="5e904-109">[CbFLATENTRYLIST](cbflatentrylist.md)、 [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="5e904-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="5e904-110">Members</span><span class="sxs-lookup"><span data-stu-id="5e904-110">Members</span></span>

<span data-ttu-id="5e904-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="5e904-111">**cEntries**</span></span>
  
> <span data-ttu-id="5e904-112">**AbEntries**メンバーが記載されている配列内の**FLATENTRY**構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="5e904-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="5e904-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="5e904-113">**cbEntries**</span></span>
  
> <span data-ttu-id="5e904-114">**AbEntries**で説明されている配列内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="5e904-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="5e904-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="5e904-115">**abEntries**</span></span>
  
> <span data-ttu-id="5e904-116">バイト配列 1 つまたは複数の**FLATENTRY**構造体を含むエンド ・ ツー ・ エンド配置します。</span><span class="sxs-lookup"><span data-stu-id="5e904-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5e904-117">注釈</span><span class="sxs-lookup"><span data-stu-id="5e904-117">Remarks</span></span>

<span data-ttu-id="5e904-118">**AbEntries**アレイでは、各**FLATENTRY**構造体が揃えられた自然な境界に揃えられます。</span><span class="sxs-lookup"><span data-stu-id="5e904-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="5e904-119">余分なバイトは、確かに自然の配置の 2 つの**FLATENTRY**構造体の間に埋め込み文字として含まれます。</span><span class="sxs-lookup"><span data-stu-id="5e904-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="5e904-120">配列内の最初の**FLATENTRY**構造体は、 **abEntries**メンバーのオフセットが 8 であるために常に、正しく配置されます。</span><span class="sxs-lookup"><span data-stu-id="5e904-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="5e904-121">次の構造体のオフセットの計算には、最初のエントリのサイズを使用して、次に 4 の倍数に切り上げられます。</span><span class="sxs-lookup"><span data-stu-id="5e904-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="5e904-122">**FLATENTRY**構造体のサイズを計算するのにには、 [CbFLATENTRY](cbflatentry.md)マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e904-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="5e904-123">などの 2 番目の**FLATENTRY**構造体は、最初のエントリのオフセットを加えた次の 4 バイトに丸められた最初のエントリの長さで構成されているオフセットから開始されます。</span><span class="sxs-lookup"><span data-stu-id="5e904-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="5e904-124">最初のエントリの長さは、 **abEntry**メンバーの長さを足したものを**cb**のメンバーの長さです。</span><span class="sxs-lookup"><span data-stu-id="5e904-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="5e904-125">次のコード サンプルでは、 **FLATENTRYLIST**構造体のオフセットを計算する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5e904-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="5e904-126">その_lpFlatEntry_が、リスト内の最初の構造体へのポインターであることと仮定します。</span><span class="sxs-lookup"><span data-stu-id="5e904-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="5e904-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e904-127">See also</span></span>

- [<span data-ttu-id="5e904-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="5e904-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="5e904-129">PidTagReplyRecipientEntries 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e904-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="5e904-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="5e904-130">MAPI Structures</span></span>](mapi-structures.md)

