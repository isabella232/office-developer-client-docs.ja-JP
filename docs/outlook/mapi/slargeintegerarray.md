---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331389"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="b053d-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="b053d-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="b053d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b053d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b053d-105">PT_MV_I8 型のプロパティを記述するために使用される[LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130)構造体の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="b053d-105">Contains an array of [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b053d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b053d-106">Header file:</span></span>  <br/> |<span data-ttu-id="b053d-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b053d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="b053d-108">Members</span><span class="sxs-lookup"><span data-stu-id="b053d-108">Members</span></span>

 <span data-ttu-id="b053d-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="b053d-109">**cValues**</span></span>
  
> <span data-ttu-id="b053d-110">**lpli**メンバーが指す配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="b053d-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="b053d-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="b053d-111">**lpli**</span></span>
  
> <span data-ttu-id="b053d-112">整数値を保持している**LARGE_INTEGER**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b053d-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b053d-113">解説</span><span class="sxs-lookup"><span data-stu-id="b053d-113">Remarks</span></span>

<span data-ttu-id="b053d-114">PT_MV_18 の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b053d-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b053d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="b053d-115">See also</span></span>



[<span data-ttu-id="b053d-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b053d-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b053d-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b053d-117">MAPI Structures</span></span>](mapi-structures.md)

