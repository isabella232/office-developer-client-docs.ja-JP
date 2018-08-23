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
ms.openlocfilehash: 6986ed7c9ab9932c5d95fcfb7f74f80088f21971
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580370"
---
# <a name="sdoublearray"></a><span data-ttu-id="4d16b-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="4d16b-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="4d16b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d16b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d16b-105">PT_MV_DOUBLE の種類のプロパティを説明するために使用する double 値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4d16b-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d16b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4d16b-106">Header file:</span></span>  <br/> |<span data-ttu-id="4d16b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d16b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="4d16b-108">Members</span><span class="sxs-lookup"><span data-stu-id="4d16b-108">Members</span></span>

 <span data-ttu-id="4d16b-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="4d16b-109">**cValues**</span></span>
  
> <span data-ttu-id="4d16b-110">**Lpdbl**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="4d16b-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="4d16b-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="4d16b-111">**lpdbl**</span></span>
  
> <span data-ttu-id="4d16b-112">Double 値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4d16b-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d16b-113">注釈</span><span class="sxs-lookup"><span data-stu-id="4d16b-113">Remarks</span></span>

<span data-ttu-id="4d16b-114">PT_MV_DOUBLE の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d16b-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d16b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d16b-115">See also</span></span>



[<span data-ttu-id="4d16b-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4d16b-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="4d16b-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="4d16b-117">MAPI Structures</span></span>](mapi-structures.md)

