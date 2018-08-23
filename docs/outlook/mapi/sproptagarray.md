---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5cfad1c75aaab9afae47de5798f9e6b7ea530940
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803986"
---
# <a name="sproptagarray"></a><span data-ttu-id="70c5f-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="70c5f-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="70c5f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70c5f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70c5f-105">プロパティ タグの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="70c5f-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70c5f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="70c5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="70c5f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70c5f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="70c5f-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="70c5f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="70c5f-109">[CbNewSPropTagArray](cbnewsproptagarray.md)、 [CbSPropTagArray](cbsproptagarray.md)、 [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="70c5f-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="70c5f-110">Members</span><span class="sxs-lookup"><span data-stu-id="70c5f-110">Members</span></span>

 <span data-ttu-id="70c5f-111">**あう**</span><span class="sxs-lookup"><span data-stu-id="70c5f-111">**cValues**</span></span>
  
> <span data-ttu-id="70c5f-112">**AulPropTag**メンバーで指定された配列内のプロパティ タグの数。</span><span class="sxs-lookup"><span data-stu-id="70c5f-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="70c5f-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="70c5f-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="70c5f-114">プロパティ タグの配列です。</span><span class="sxs-lookup"><span data-stu-id="70c5f-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70c5f-115">注釈</span><span class="sxs-lookup"><span data-stu-id="70c5f-115">Remarks</span></span>

<span data-ttu-id="70c5f-116">プロパティ タグは、2 つの部分で構成される 32 ビット符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="70c5f-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="70c5f-117">上位 16 ビットの識別子です。</span><span class="sxs-lookup"><span data-stu-id="70c5f-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="70c5f-118">下位 16 ビットのタイプです。</span><span class="sxs-lookup"><span data-stu-id="70c5f-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="70c5f-119">識別子は、特定の範囲内の数値です。</span><span class="sxs-lookup"><span data-stu-id="70c5f-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="70c5f-120">MAPI は、プロパティの使用および保守の責任者を記述する識別子の範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="70c5f-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="70c5f-121">MAPI では、Mapitags.h ヘッダー ファイルでサポートされているプロパティ タグのそれぞれの制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="70c5f-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="70c5f-122">型は、プロパティの値の形式を示します。</span><span class="sxs-lookup"><span data-stu-id="70c5f-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="70c5f-123">MAPI では、Mapidefs.h ヘッダー ファイルでサポートされているプロパティの型のそれぞれの定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="70c5f-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="70c5f-124">プロパティ タグとそのコンポーネントの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="70c5f-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="70c5f-125">MAPI プロパティ タグ</span><span class="sxs-lookup"><span data-stu-id="70c5f-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="70c5f-126">MAPI プロパティ識別子の概要</span><span class="sxs-lookup"><span data-stu-id="70c5f-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="70c5f-127">MAPI プロパティの型の概要</span><span class="sxs-lookup"><span data-stu-id="70c5f-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="70c5f-128">単一値および複数値を持つプロパティの型の完全なリストは、[プロパティの識別子と型](property-identifiers-and-types.md)は、付録を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70c5f-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70c5f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="70c5f-129">See also</span></span>



[<span data-ttu-id="70c5f-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="70c5f-130">MAPI Structures</span></span>](mapi-structures.md)

