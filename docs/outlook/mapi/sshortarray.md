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
ms.openlocfilehash: 59911531b6d8f9c094ef8563510aaa176e3a63b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804010"
---
# <a name="sshortarray"></a><span data-ttu-id="6f15f-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="6f15f-103">SShortArray</span></span>

  
  
<span data-ttu-id="6f15f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f15f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f15f-105">PT_MV_SHORT の種類のプロパティを説明するために使用する符号なし整数値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f15f-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f15f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6f15f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6f15f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f15f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="6f15f-108">Members</span><span class="sxs-lookup"><span data-stu-id="6f15f-108">Members</span></span>

 <span data-ttu-id="6f15f-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="6f15f-109">**cValues**</span></span>
  
> <span data-ttu-id="6f15f-110">**Lpi**のメンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="6f15f-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="6f15f-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="6f15f-111">**lpi**</span></span>
  
> <span data-ttu-id="6f15f-112">符号なし整数値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6f15f-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f15f-113">注釈</span><span class="sxs-lookup"><span data-stu-id="6f15f-113">Remarks</span></span>

<span data-ttu-id="6f15f-114">PT_MV_SHORT およびその他のプロパティの種類の詳細については、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f15f-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f15f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6f15f-115">See also</span></span>



[<span data-ttu-id="6f15f-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6f15f-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6f15f-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="6f15f-117">MAPI Structures</span></span>](mapi-structures.md)

