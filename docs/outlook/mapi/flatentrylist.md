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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800071"
---
# <a name="flatentrylist"></a><span data-ttu-id="b0a7b-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="b0a7b-103">FLATENTRYLIST</span></span>

<span data-ttu-id="b0a7b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0a7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0a7b-105">[FLATENTRY](flatentry.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0a7b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b0a7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0a7b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0a7b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b0a7b-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="b0a7b-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b0a7b-109">[CbFLATENTRYLIST](cbflatentrylist.md)、 [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="b0a7b-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="b0a7b-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="b0a7b-110">Members</span></span>

<span data-ttu-id="b0a7b-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="b0a7b-111">**cEntries**</span></span>
  
> <span data-ttu-id="b0a7b-112">**AbEntries**メンバーが記載されている配列内の**FLATENTRY**構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="b0a7b-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="b0a7b-113">**cbEntries**</span></span>
  
> <span data-ttu-id="b0a7b-114">**AbEntries**で説明されている配列内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="b0a7b-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="b0a7b-115">**abEntries**</span></span>
  
> <span data-ttu-id="b0a7b-116">バイト配列 1 つまたは複数の**FLATENTRY**構造体を含むエンド ・ ツー ・ エンド配置します。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b0a7b-117">備考</span><span class="sxs-lookup"><span data-stu-id="b0a7b-117">Remarks</span></span>

<span data-ttu-id="b0a7b-118">**AbEntries**アレイでは、各**FLATENTRY**構造体が揃えられた自然な境界に揃えられます。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="b0a7b-119">余分なバイトは、確かに自然の配置の 2 つの**FLATENTRY**構造体の間に埋め込み文字として含まれます。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="b0a7b-120">配列内の最初の**FLATENTRY**構造体は、 **abEntries**メンバーのオフセットが 8 であるために常に、正しく配置されます。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="b0a7b-121">次の構造体のオフセットの計算には、最初のエントリのサイズを使用して、次に 4 の倍数に切り上げられます。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="b0a7b-122">**FLATENTRY**構造体のサイズを計算するのにには、 [CbFLATENTRY](cbflatentry.md)マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="b0a7b-123">などの 2 番目の**FLATENTRY**構造体は、最初のエントリのオフセットを加えた次の 4 バイトに丸められた最初のエントリの長さで構成されているオフセットから開始されます。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="b0a7b-124">最初のエントリの長さは、 **abEntry**メンバーの長さを足したものを**cb**のメンバーの長さです。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="b0a7b-125">次のコード サンプルでは、 **FLATENTRYLIST**構造体のオフセットを計算する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="b0a7b-126">その_lpFlatEntry_が、リスト内の最初の構造体へのポインターであることと仮定します。</span><span class="sxs-lookup"><span data-stu-id="b0a7b-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="b0a7b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0a7b-127">See also</span></span>

- [<span data-ttu-id="b0a7b-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="b0a7b-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="b0a7b-129">PidTagReplyRecipientEntries の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b0a7b-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="b0a7b-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b0a7b-130">MAPI Structures</span></span>](mapi-structures.md)

