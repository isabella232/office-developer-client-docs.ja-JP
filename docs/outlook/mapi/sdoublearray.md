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
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803853"
---
# <a name="sdoublearray"></a><span data-ttu-id="73a7e-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="73a7e-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="73a7e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73a7e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73a7e-105">PT_MV_DOUBLE の種類のプロパティを説明するために使用する double 値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="73a7e-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73a7e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="73a7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="73a7e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="73a7e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="73a7e-108">Members</span><span class="sxs-lookup"><span data-stu-id="73a7e-108">Members</span></span>

 <span data-ttu-id="73a7e-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="73a7e-109">**cValues**</span></span>
  
> <span data-ttu-id="73a7e-110">**Lpdbl**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="73a7e-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="73a7e-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="73a7e-111">**lpdbl**</span></span>
  
> <span data-ttu-id="73a7e-112">Double 値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="73a7e-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73a7e-113">注釈</span><span class="sxs-lookup"><span data-stu-id="73a7e-113">Remarks</span></span>

<span data-ttu-id="73a7e-114">PT_MV_DOUBLE の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="73a7e-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="73a7e-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="73a7e-115">See also</span></span>



[<span data-ttu-id="73a7e-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="73a7e-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="73a7e-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="73a7e-117">MAPI Structures</span></span>](mapi-structures.md)

