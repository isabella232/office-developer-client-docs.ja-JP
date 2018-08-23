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
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803943"
---
# <a name="slongarray"></a><span data-ttu-id="1444e-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="1444e-103">SLongArray</span></span>

  
  
<span data-ttu-id="1444e-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1444e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1444e-105">PT_MV_LONG の種類のプロパティを説明するために使用する long 型の値型の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1444e-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1444e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1444e-106">Header file:</span></span>  <br/> |<span data-ttu-id="1444e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1444e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="1444e-108">Members</span><span class="sxs-lookup"><span data-stu-id="1444e-108">Members</span></span>

 <span data-ttu-id="1444e-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="1444e-109">**cValues**</span></span>
  
> <span data-ttu-id="1444e-110">**Lpl**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="1444e-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="1444e-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="1444e-111">**lpl**</span></span>
  
> <span data-ttu-id="1444e-112">LONG 値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1444e-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1444e-113">注釈</span><span class="sxs-lookup"><span data-stu-id="1444e-113">Remarks</span></span>

<span data-ttu-id="1444e-114">PT_MV_LONG の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1444e-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1444e-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="1444e-115">See also</span></span>



[<span data-ttu-id="1444e-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1444e-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1444e-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="1444e-117">MAPI Structures</span></span>](mapi-structures.md)

