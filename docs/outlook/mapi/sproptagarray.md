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
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344437"
---
# <a name="sproptagarray"></a><span data-ttu-id="4e750-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4e750-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="4e750-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e750-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e750-105">プロパティタグの配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="4e750-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e750-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4e750-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e750-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e750-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4e750-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="4e750-108">Related macros:</span></span>  <br/> |<span data-ttu-id="4e750-109">[CbNewSPropTagArray](cbnewsproptagarray.md)、 [CbSPropTagArray](cbsproptagarray.md)、 [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="4e750-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="4e750-110">Members</span><span class="sxs-lookup"><span data-stu-id="4e750-110">Members</span></span>

 <span data-ttu-id="4e750-111">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="4e750-111">**cValues**</span></span>
  
> <span data-ttu-id="4e750-112">**aulPropTag**メンバーによって示される、配列内のプロパティタグの数。</span><span class="sxs-lookup"><span data-stu-id="4e750-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="4e750-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="4e750-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="4e750-114">プロパティタグの配列。</span><span class="sxs-lookup"><span data-stu-id="4e750-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e750-115">解説</span><span class="sxs-lookup"><span data-stu-id="4e750-115">Remarks</span></span>

<span data-ttu-id="4e750-116">property タグは、2つの部分で構成される32ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="4e750-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="4e750-117">上位16ビットの識別子。</span><span class="sxs-lookup"><span data-stu-id="4e750-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="4e750-118">ローオーダー16ビットの型。</span><span class="sxs-lookup"><span data-stu-id="4e750-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="4e750-119">識別子は、特定の範囲の数値です。</span><span class="sxs-lookup"><span data-stu-id="4e750-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="4e750-120">MAPI は、識別子の範囲を定義して、プロパティがどのように使用され、保持する責任者を示します。</span><span class="sxs-lookup"><span data-stu-id="4e750-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="4e750-121">MAPI は、Mapitags ヘッダーファイルでサポートされている各プロパティタグに対する制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="4e750-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="4e750-122">この型は、プロパティの値の形式を示します。</span><span class="sxs-lookup"><span data-stu-id="4e750-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="4e750-123">MAPI は、mapidefs.h ヘッダーファイルでサポートされている各プロパティの種類に対して定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="4e750-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="4e750-124">プロパティタグとそのコンポーネントの詳細については、以下のいずれかのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e750-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="4e750-125">MAPI プロパティタグ</span><span class="sxs-lookup"><span data-stu-id="4e750-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="4e750-126">MAPI プロパティ識別子の概要</span><span class="sxs-lookup"><span data-stu-id="4e750-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="4e750-127">MAPI プロパティの種類の概要</span><span class="sxs-lookup"><span data-stu-id="4e750-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="4e750-128">単一値および複数値のプロパティの種類の完全な一覧については、付録、[プロパティの識別子と型](property-identifiers-and-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4e750-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e750-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="4e750-129">See also</span></span>



[<span data-ttu-id="4e750-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="4e750-130">MAPI Structures</span></span>](mapi-structures.md)

