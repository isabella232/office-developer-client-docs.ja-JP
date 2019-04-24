---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361153"
---
# <a name="slpstrarray"></a><span data-ttu-id="004e9-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="004e9-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="004e9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="004e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="004e9-105">PT_MV_STRING8 型のプロパティを記述するために使用される文字列値の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="004e9-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="004e9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="004e9-106">Header file:</span></span>  <br/> |<span data-ttu-id="004e9-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="004e9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="004e9-108">Members</span><span class="sxs-lookup"><span data-stu-id="004e9-108">Members</span></span>

 <span data-ttu-id="004e9-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="004e9-109">**cValues**</span></span>
  
> <span data-ttu-id="004e9-110">**lppszA**メンバーが指す配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="004e9-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="004e9-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="004e9-111">**lppszA**</span></span>
  
> <span data-ttu-id="004e9-112">null で終了した8ビット文字の文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="004e9-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="004e9-113">解説</span><span class="sxs-lookup"><span data-stu-id="004e9-113">Remarks</span></span>

<span data-ttu-id="004e9-114">PT_MV_STRING8 の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="004e9-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="004e9-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="004e9-115">See also</span></span>



[<span data-ttu-id="004e9-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="004e9-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="004e9-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="004e9-117">MAPI Structures</span></span>](mapi-structures.md)

