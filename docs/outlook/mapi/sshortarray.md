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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429615"
---
# <a name="sshortarray"></a><span data-ttu-id="3b6be-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="3b6be-103">SShortArray</span></span>

  
  
<span data-ttu-id="3b6be-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b6be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b6be-105">型のプロパティを記述するために使用される符号なし整数値の配列をPT_MV_SHORT。</span><span class="sxs-lookup"><span data-stu-id="3b6be-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b6be-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3b6be-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b6be-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b6be-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="3b6be-108">Members</span><span class="sxs-lookup"><span data-stu-id="3b6be-108">Members</span></span>

 <span data-ttu-id="3b6be-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3b6be-109">**cValues**</span></span>
  
> <span data-ttu-id="3b6be-110">lpi メンバーが指す配列内の **値の** 数。</span><span class="sxs-lookup"><span data-stu-id="3b6be-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="3b6be-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="3b6be-111">**lpi**</span></span>
  
> <span data-ttu-id="3b6be-112">符号なし整数値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b6be-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3b6be-113">注釈</span><span class="sxs-lookup"><span data-stu-id="3b6be-113">Remarks</span></span>

<span data-ttu-id="3b6be-114">プロパティおよび他のプロパティPT_MV_SHORT詳細については [、「Property Types」を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="3b6be-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b6be-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b6be-115">See also</span></span>



[<span data-ttu-id="3b6be-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3b6be-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3b6be-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="3b6be-117">MAPI Structures</span></span>](mapi-structures.md)

