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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799876"
---
# <a name="currency"></a><span data-ttu-id="898bf-103">CURRENCY</span><span class="sxs-lookup"><span data-stu-id="898bf-103">CURRENCY</span></span>

  
  
<span data-ttu-id="898bf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="898bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="898bf-105">通貨の値を表す 64 ビットの符号付き整数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="898bf-105">Contains a signed 64-bit integer representing a currency value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="898bf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="898bf-106">Header file:</span></span>  <br/> |<span data-ttu-id="898bf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="898bf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a><span data-ttu-id="898bf-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="898bf-108">Members</span></span>

 <span data-ttu-id="898bf-109">**Lo**</span><span class="sxs-lookup"><span data-stu-id="898bf-109">**Lo**</span></span>
  
> <span data-ttu-id="898bf-110">通貨型の値の下位 32 ビット。</span><span class="sxs-lookup"><span data-stu-id="898bf-110">Low-order 32 bits of the currency value.</span></span> 
    
 <span data-ttu-id="898bf-111">**こんにちは**</span><span class="sxs-lookup"><span data-stu-id="898bf-111">**Hi**</span></span>
  
> <span data-ttu-id="898bf-112">通貨型の値の上位の 32 ビットです。</span><span class="sxs-lookup"><span data-stu-id="898bf-112">High-order 32 bits of the currency value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="898bf-113">備考</span><span class="sxs-lookup"><span data-stu-id="898bf-113">Remarks</span></span>

<span data-ttu-id="898bf-114">**通貨**の構造は、小数点の右側に 4 桁の 10 進数の位取り整数表現です。</span><span class="sxs-lookup"><span data-stu-id="898bf-114">The **CURRENCY** structure is a scaled integer representation of a decimal number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="898bf-115">327500 の格納された値は 32.7500 の通貨値を表すものとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="898bf-115">For example, a stored value of 327500 is to be construed as representing a currency value of 32.7500.</span></span> 
  
<span data-ttu-id="898bf-116">**通貨**の構造体を使用して、PT_CURRENCY の種類のプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="898bf-116">The **CURRENCY** structure is used to describe a property of type PT_CURRENCY.</span></span> <span data-ttu-id="898bf-117">プロパティの型については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="898bf-117">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="898bf-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="898bf-118">See also</span></span>



[<span data-ttu-id="898bf-119">SPropValue</span><span class="sxs-lookup"><span data-stu-id="898bf-119">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="898bf-120">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="898bf-120">MAPI Structures</span></span>](mapi-structures.md)

