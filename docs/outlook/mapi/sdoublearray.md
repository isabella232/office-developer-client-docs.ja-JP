---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439269"
---
# <a name="sdoublearray"></a><span data-ttu-id="f9d84-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="f9d84-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="f9d84-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9d84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9d84-105">型のプロパティを記述するために使用される倍数の配列が含PT_MV_DOUBLE。</span><span class="sxs-lookup"><span data-stu-id="f9d84-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9d84-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f9d84-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9d84-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9d84-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="f9d84-108">Members</span><span class="sxs-lookup"><span data-stu-id="f9d84-108">Members</span></span>

 <span data-ttu-id="f9d84-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f9d84-109">**cValues**</span></span>
  
> <span data-ttu-id="f9d84-110">**lpdbl** メンバーが指す配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="f9d84-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="f9d84-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="f9d84-111">**lpdbl**</span></span>
  
> <span data-ttu-id="f9d84-112">倍数の値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f9d84-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9d84-113">注釈</span><span class="sxs-lookup"><span data-stu-id="f9d84-113">Remarks</span></span>

<span data-ttu-id="f9d84-114">プロパティの詳細については、「PT_MV_DOUBLEプロパティ [の種類の一覧」を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f9d84-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9d84-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9d84-115">See also</span></span>



[<span data-ttu-id="f9d84-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f9d84-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f9d84-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f9d84-117">MAPI Structures</span></span>](mapi-structures.md)

