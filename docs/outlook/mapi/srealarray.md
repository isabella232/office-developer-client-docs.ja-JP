---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429874"
---
# <a name="srealarray"></a><span data-ttu-id="8c436-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="8c436-103">SRealArray</span></span>

  
  
<span data-ttu-id="8c436-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c436-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c436-105">PT_MV_R4 型のプロパティを記述するために使用される float 値の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="8c436-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c436-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8c436-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c436-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c436-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="8c436-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="8c436-108">Members</span></span>

 <span data-ttu-id="8c436-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="8c436-109">**cValues**</span></span>
  
> <span data-ttu-id="8c436-110">**lpflt**メンバーが指す配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="8c436-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="8c436-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="8c436-111">**lpflt**</span></span>
  
> <span data-ttu-id="8c436-112">浮動小数点型の値の配列へのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="8c436-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c436-113">注釈</span><span class="sxs-lookup"><span data-stu-id="8c436-113">Remarks</span></span>

<span data-ttu-id="8c436-114">PT_MV_R4 プロパティの種類の詳細については、「[プロパティの種類](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c436-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8c436-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c436-115">See also</span></span>



[<span data-ttu-id="8c436-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8c436-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8c436-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="8c436-117">MAPI Structures</span></span>](mapi-structures.md)

