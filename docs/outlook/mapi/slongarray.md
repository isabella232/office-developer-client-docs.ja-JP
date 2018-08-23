---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a44974accea30b5d1406c9cc74570012f61639e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580650"
---
# <a name="slongarray"></a><span data-ttu-id="7568a-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="7568a-103">SLongArray</span></span>

  
  
<span data-ttu-id="7568a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7568a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7568a-105">PT_MV_LONG の種類のプロパティを説明するために使用する long 型の値型の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7568a-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7568a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7568a-106">Header file:</span></span>  <br/> |<span data-ttu-id="7568a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7568a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="7568a-108">Members</span><span class="sxs-lookup"><span data-stu-id="7568a-108">Members</span></span>

 <span data-ttu-id="7568a-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="7568a-109">**cValues**</span></span>
  
> <span data-ttu-id="7568a-110">**Lpl**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="7568a-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="7568a-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="7568a-111">**lpl**</span></span>
  
> <span data-ttu-id="7568a-112">LONG 値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7568a-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7568a-113">注釈</span><span class="sxs-lookup"><span data-stu-id="7568a-113">Remarks</span></span>

<span data-ttu-id="7568a-114">PT_MV_LONG の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7568a-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7568a-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="7568a-115">See also</span></span>



[<span data-ttu-id="7568a-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7568a-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7568a-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="7568a-117">MAPI Structures</span></span>](mapi-structures.md)

