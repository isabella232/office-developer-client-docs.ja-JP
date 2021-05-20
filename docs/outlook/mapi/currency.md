---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431121"
---
# <a name="currency"></a><span data-ttu-id="9c2bd-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="9c2bd-103">CURRENCY</span></span>

  
  
<span data-ttu-id="9c2bd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c2bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c2bd-105">通貨値を表す符号付き 64 ビット整数を含む。</span><span class="sxs-lookup"><span data-stu-id="9c2bd-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c2bd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9c2bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c2bd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c2bd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="9c2bd-108">Members</span><span class="sxs-lookup"><span data-stu-id="9c2bd-108">Members</span></span>

 <span data-ttu-id="9c2bd-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="9c2bd-109">**Lo**</span></span>
  
> <span data-ttu-id="9c2bd-110">通貨値の低次 32 ビット。</span><span class="sxs-lookup"><span data-stu-id="9c2bd-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="9c2bd-111">**こんにちは**</span><span class="sxs-lookup"><span data-stu-id="9c2bd-111">**Hi**</span></span>
  
> <span data-ttu-id="9c2bd-112">通貨値の高次 32 ビット。</span><span class="sxs-lookup"><span data-stu-id="9c2bd-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c2bd-113">注釈</span><span class="sxs-lookup"><span data-stu-id="9c2bd-113">Remarks</span></span>

<span data-ttu-id="9c2bd-114">**CURRENCY 構造体** は、小数点の右側に 4 桁の数字を持つ 10 進数の拡大縮小整数表現です。</span><span class="sxs-lookup"><span data-stu-id="9c2bd-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="9c2bd-115">たとえば、格納されている値 327500 は、通貨値 32.7500 を表すと解釈されます。</span><span class="sxs-lookup"><span data-stu-id="9c2bd-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="9c2bd-116">**CURRENCY 構造体** は、プロパティの種類のプロパティを記述するために使用PT_CURRENCY。</span><span class="sxs-lookup"><span data-stu-id="9c2bd-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="9c2bd-117">プロパティの種類の詳細については [、「MAPI プロパティの種類の概要」を参照してください](mapi-property-type-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="9c2bd-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c2bd-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c2bd-118">See also</span></span>



[<span data-ttu-id="9c2bd-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9c2bd-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="9c2bd-120">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9c2bd-120">MAPI Structures</span></span>](mapi-structures.md)

