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
ms.openlocfilehash: 4d6785783f69857bd93f3c5818983e832e16af05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803951"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="0f9c8-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="0f9c8-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="0f9c8-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f9c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f9c8-105">PT_MV_I8 の種類のプロパティを説明するために使用する[LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f9c8-105">Contains an array of [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f9c8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0f9c8-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f9c8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f9c8-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="0f9c8-108">Members</span><span class="sxs-lookup"><span data-stu-id="0f9c8-108">Members</span></span>

 <span data-ttu-id="0f9c8-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="0f9c8-109">**cValues**</span></span>
  
> <span data-ttu-id="0f9c8-110">**Lpli**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="0f9c8-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="0f9c8-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="0f9c8-111">**lpli**</span></span>
  
> <span data-ttu-id="0f9c8-112">整数値を保持している**LARGE_INTEGER**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0f9c8-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0f9c8-113">注釈</span><span class="sxs-lookup"><span data-stu-id="0f9c8-113">Remarks</span></span>

<span data-ttu-id="0f9c8-114">PT_MV_18 の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f9c8-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0f9c8-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f9c8-115">See also</span></span>



[<span data-ttu-id="0f9c8-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0f9c8-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0f9c8-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0f9c8-117">MAPI Structures</span></span>](mapi-structures.md)

