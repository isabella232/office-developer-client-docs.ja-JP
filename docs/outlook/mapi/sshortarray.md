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
# <a name="sshortarray"></a><span data-ttu-id="ffa0c-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="ffa0c-103">SShortArray</span></span>

  
  
<span data-ttu-id="ffa0c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffa0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffa0c-105">PT_MV_SHORT 型のプロパティを記述するために使用される、符号なし整数値の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="ffa0c-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffa0c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ffa0c-106">Header file:</span></span>  <br/> |<span data-ttu-id="ffa0c-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffa0c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="ffa0c-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="ffa0c-108">Members</span></span>

 <span data-ttu-id="ffa0c-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="ffa0c-109">**cValues**</span></span>
  
> <span data-ttu-id="ffa0c-110">**lpi**メンバーが指す配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="ffa0c-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="ffa0c-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="ffa0c-111">**lpi**</span></span>
  
> <span data-ttu-id="ffa0c-112">符号なし整数値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ffa0c-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ffa0c-113">注釈</span><span class="sxs-lookup"><span data-stu-id="ffa0c-113">Remarks</span></span>

<span data-ttu-id="ffa0c-114">PT_MV_SHORT およびその他のプロパティの種類の詳細については、「[プロパティの種類](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffa0c-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ffa0c-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="ffa0c-115">See also</span></span>



[<span data-ttu-id="ffa0c-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ffa0c-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="ffa0c-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ffa0c-117">MAPI Structures</span></span>](mapi-structures.md)

