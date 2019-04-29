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
# <a name="currency"></a><span data-ttu-id="a8858-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="a8858-103">CURRENCY</span></span>

  
  
<span data-ttu-id="a8858-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8858-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8858-105">通貨値を表す、符号付きの64ビット整数を含みます。</span><span class="sxs-lookup"><span data-stu-id="a8858-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8858-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a8858-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8858-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8858-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="a8858-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="a8858-108">Members</span></span>

 <span data-ttu-id="a8858-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="a8858-109">**Lo**</span></span>
  
> <span data-ttu-id="a8858-110">通貨値の低順位32ビット。</span><span class="sxs-lookup"><span data-stu-id="a8858-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="a8858-111">**こんにちは**</span><span class="sxs-lookup"><span data-stu-id="a8858-111">**Hi**</span></span>
  
> <span data-ttu-id="a8858-112">通貨値の上位32ビット。</span><span class="sxs-lookup"><span data-stu-id="a8858-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8858-113">注釈</span><span class="sxs-lookup"><span data-stu-id="a8858-113">Remarks</span></span>

<span data-ttu-id="a8858-114">**通貨**構造は、小数点の右側に4桁の10進数を使用した10進数の整数表現です。</span><span class="sxs-lookup"><span data-stu-id="a8858-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="a8858-115">たとえば、327500の格納された値は、32.7500 の通貨値を表すものとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="a8858-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="a8858-116">**通貨**構造は、PT_CURRENCY 型のプロパティを記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a8858-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="a8858-117">プロパティの種類の詳細については、「 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8858-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8858-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8858-118">See also</span></span>



[<span data-ttu-id="a8858-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a8858-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a8858-120">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="a8858-120">MAPI Structures</span></span>](mapi-structures.md)

