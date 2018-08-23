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
ms.openlocfilehash: ccad74a9f2553bf29af124821c6d6a87dcde3303
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572873"
---
# <a name="slpstrarray"></a><span data-ttu-id="8c571-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="8c571-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="8c571-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c571-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c571-105">PT_MV_STRING8 の種類のプロパティを説明するために使用する文字列値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8c571-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c571-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8c571-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c571-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c571-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="8c571-108">Members</span><span class="sxs-lookup"><span data-stu-id="8c571-108">Members</span></span>

 <span data-ttu-id="8c571-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="8c571-109">**cValues**</span></span>
  
> <span data-ttu-id="8c571-110">**LppszA**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="8c571-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="8c571-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="8c571-111">**lppszA**</span></span>
  
> <span data-ttu-id="8c571-112">8 ビット文字の null 終了文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8c571-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c571-113">注釈</span><span class="sxs-lookup"><span data-stu-id="8c571-113">Remarks</span></span>

<span data-ttu-id="8c571-114">PT_MV_STRING8 の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c571-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c571-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c571-115">See also</span></span>



[<span data-ttu-id="8c571-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8c571-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8c571-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="8c571-117">MAPI Structures</span></span>](mapi-structures.md)

