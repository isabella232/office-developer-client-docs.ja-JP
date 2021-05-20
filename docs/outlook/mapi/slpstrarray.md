---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435909"
---
# <a name="slpstrarray"></a><span data-ttu-id="04d03-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="04d03-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="04d03-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04d03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04d03-105">型のプロパティを記述するために使用される文字列値の配列が含PT_MV_STRING8。</span><span class="sxs-lookup"><span data-stu-id="04d03-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04d03-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="04d03-106">Header file:</span></span>  <br/> |<span data-ttu-id="04d03-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04d03-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="04d03-108">Members</span><span class="sxs-lookup"><span data-stu-id="04d03-108">Members</span></span>

 <span data-ttu-id="04d03-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="04d03-109">**cValues**</span></span>
  
> <span data-ttu-id="04d03-110">lppszA メンバーが指す配列 **内の値の** 数。</span><span class="sxs-lookup"><span data-stu-id="04d03-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="04d03-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="04d03-111">**lppszA**</span></span>
  
> <span data-ttu-id="04d03-112">null-ended 8 ビット文字文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="04d03-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04d03-113">注釈</span><span class="sxs-lookup"><span data-stu-id="04d03-113">Remarks</span></span>

<span data-ttu-id="04d03-114">プロパティの詳細については、「PT_MV_STRING8の [種類」を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="04d03-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="04d03-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="04d03-115">See also</span></span>



[<span data-ttu-id="04d03-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="04d03-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="04d03-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="04d03-117">MAPI Structures</span></span>](mapi-structures.md)

