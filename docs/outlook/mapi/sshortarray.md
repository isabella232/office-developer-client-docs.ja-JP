---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573034"
---
# <a name="sshortarray"></a><span data-ttu-id="e985c-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="e985c-103">SShortArray</span></span>

  
  
<span data-ttu-id="e985c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e985c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e985c-105">PT_MV_SHORT の種類のプロパティを説明するために使用する符号なし整数値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e985c-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e985c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e985c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e985c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e985c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="e985c-108">Members</span><span class="sxs-lookup"><span data-stu-id="e985c-108">Members</span></span>

 <span data-ttu-id="e985c-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="e985c-109">**cValues**</span></span>
  
> <span data-ttu-id="e985c-110">**Lpi**のメンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="e985c-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="e985c-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="e985c-111">**lpi**</span></span>
  
> <span data-ttu-id="e985c-112">符号なし整数値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e985c-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e985c-113">注釈</span><span class="sxs-lookup"><span data-stu-id="e985c-113">Remarks</span></span>

<span data-ttu-id="e985c-114">PT_MV_SHORT およびその他のプロパティの種類の詳細については、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e985c-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e985c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e985c-115">See also</span></span>



[<span data-ttu-id="e985c-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e985c-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="e985c-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="e985c-117">MAPI Structures</span></span>](mapi-structures.md)

