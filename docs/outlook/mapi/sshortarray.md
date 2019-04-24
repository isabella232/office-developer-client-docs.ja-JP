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
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344500"
---
# <a name="sshortarray"></a><span data-ttu-id="8376b-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="8376b-103">SShortArray</span></span>

  
  
<span data-ttu-id="8376b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8376b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8376b-105">PT_MV_SHORT 型のプロパティを記述するために使用される、符号なし整数値の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="8376b-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8376b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8376b-106">Header file:</span></span>  <br/> |<span data-ttu-id="8376b-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8376b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="8376b-108">Members</span><span class="sxs-lookup"><span data-stu-id="8376b-108">Members</span></span>

 <span data-ttu-id="8376b-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="8376b-109">**cValues**</span></span>
  
> <span data-ttu-id="8376b-110">**lpi**メンバーが指す配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="8376b-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="8376b-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="8376b-111">**lpi**</span></span>
  
> <span data-ttu-id="8376b-112">符号なし整数値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8376b-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8376b-113">解説</span><span class="sxs-lookup"><span data-stu-id="8376b-113">Remarks</span></span>

<span data-ttu-id="8376b-114">PT_MV_SHORT およびその他のプロパティの種類の詳細については、「[プロパティの種類](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8376b-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8376b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="8376b-115">See also</span></span>



[<span data-ttu-id="8376b-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8376b-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8376b-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="8376b-117">MAPI Structures</span></span>](mapi-structures.md)

