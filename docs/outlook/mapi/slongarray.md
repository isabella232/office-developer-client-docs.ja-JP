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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414530"
---
# <a name="slongarray"></a><span data-ttu-id="214e1-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="214e1-103">SLongArray</span></span>

  
  
<span data-ttu-id="214e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="214e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="214e1-105">PT_MV_LONG 型のプロパティを記述するために使用される LONG 値型の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="214e1-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="214e1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="214e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="214e1-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="214e1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="214e1-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="214e1-108">Members</span></span>

 <span data-ttu-id="214e1-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="214e1-109">**cValues**</span></span>
  
> <span data-ttu-id="214e1-110">**lpl**メンバによって示された配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="214e1-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="214e1-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="214e1-111">**lpl**</span></span>
  
> <span data-ttu-id="214e1-112">長整数型 (LONG) の値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="214e1-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="214e1-113">注釈</span><span class="sxs-lookup"><span data-stu-id="214e1-113">Remarks</span></span>

<span data-ttu-id="214e1-114">PT_MV_LONG の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="214e1-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="214e1-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="214e1-115">See also</span></span>



[<span data-ttu-id="214e1-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="214e1-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="214e1-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="214e1-117">MAPI Structures</span></span>](mapi-structures.md)

