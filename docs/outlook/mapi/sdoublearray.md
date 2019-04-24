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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 91440d619c8ad8a64b2bac7463a26d9c196a3c0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339733"
---
# <a name="sdoublearray"></a><span data-ttu-id="98ce8-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="98ce8-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="98ce8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98ce8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98ce8-105">PT_MV_DOUBLE 型のプロパティを記述するために使用される倍精度浮動小数点数の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="98ce8-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98ce8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="98ce8-106">Header file:</span></span>  <br/> |<span data-ttu-id="98ce8-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98ce8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="98ce8-108">Members</span><span class="sxs-lookup"><span data-stu-id="98ce8-108">Members</span></span>

 <span data-ttu-id="98ce8-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="98ce8-109">**cValues**</span></span>
  
> <span data-ttu-id="98ce8-110">lpsingleメンバーが指す配列内の値の\*\*\*\* 数。</span><span class="sxs-lookup"><span data-stu-id="98ce8-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="98ce8-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="98ce8-111">**lpdbl**</span></span>
  
> <span data-ttu-id="98ce8-112">倍精度浮動小数点型の値の配列へのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="98ce8-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98ce8-113">解説</span><span class="sxs-lookup"><span data-stu-id="98ce8-113">Remarks</span></span>

<span data-ttu-id="98ce8-114">PT_MV_DOUBLE の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98ce8-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98ce8-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="98ce8-115">See also</span></span>



[<span data-ttu-id="98ce8-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="98ce8-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="98ce8-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="98ce8-117">MAPI Structures</span></span>](mapi-structures.md)

