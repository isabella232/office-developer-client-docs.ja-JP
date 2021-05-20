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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430701"
---
# <a name="sproptagarray"></a><span data-ttu-id="229d2-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="229d2-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="229d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="229d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="229d2-105">プロパティ タグの配列を含む。</span><span class="sxs-lookup"><span data-stu-id="229d2-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="229d2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="229d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="229d2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="229d2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="229d2-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="229d2-108">Related macros:</span></span>  <br/> |<span data-ttu-id="229d2-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="229d2-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="229d2-110">Members</span><span class="sxs-lookup"><span data-stu-id="229d2-110">Members</span></span>

 <span data-ttu-id="229d2-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="229d2-111">**cValues**</span></span>
  
> <span data-ttu-id="229d2-112">**aulPropTag** メンバーによって示される配列内のプロパティ タグの数。</span><span class="sxs-lookup"><span data-stu-id="229d2-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="229d2-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="229d2-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="229d2-114">プロパティ タグの配列。</span><span class="sxs-lookup"><span data-stu-id="229d2-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="229d2-115">注釈</span><span class="sxs-lookup"><span data-stu-id="229d2-115">Remarks</span></span>

<span data-ttu-id="229d2-116">プロパティ タグは、2 つの部分で構成される 32 ビットの符号なし整数です。</span><span class="sxs-lookup"><span data-stu-id="229d2-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="229d2-117">高次 16 ビットの識別子。</span><span class="sxs-lookup"><span data-stu-id="229d2-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="229d2-118">低次 16 ビットの型。</span><span class="sxs-lookup"><span data-stu-id="229d2-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="229d2-119">識別子は、特定の範囲の数値です。</span><span class="sxs-lookup"><span data-stu-id="229d2-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="229d2-120">MAPI では、プロパティの使用および管理の責任者を示す識別子の範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="229d2-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="229d2-121">MAPI は、Mapitags.h ヘッダー ファイルでサポートする各プロパティ タグの制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="229d2-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="229d2-122">型は、プロパティの値の形式を示します。</span><span class="sxs-lookup"><span data-stu-id="229d2-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="229d2-123">MAPI は、Mapidefs.h ヘッダー ファイルでサポートする各プロパティの種類の定数を定義します。</span><span class="sxs-lookup"><span data-stu-id="229d2-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="229d2-124">プロパティ タグとそのコンポーネントの詳細については、次のいずれかのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="229d2-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="229d2-125">MAPI プロパティ のタグ</span><span class="sxs-lookup"><span data-stu-id="229d2-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="229d2-126">MAPI プロパティ識別子の概要</span><span class="sxs-lookup"><span data-stu-id="229d2-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="229d2-127">MAPI プロパティの種類の概要</span><span class="sxs-lookup"><span data-stu-id="229d2-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="229d2-128">単一値および複数値プロパティの種類の完全な一覧については、付録「プロパティ識別子と型」 [を参照してください](property-identifiers-and-types.md)。</span><span class="sxs-lookup"><span data-stu-id="229d2-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="229d2-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="229d2-129">See also</span></span>



[<span data-ttu-id="229d2-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="229d2-130">MAPI Structures</span></span>](mapi-structures.md)

