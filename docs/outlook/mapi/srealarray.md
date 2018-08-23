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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c7ce2805248bf91ce7da071c67ece28a5b8ca07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564284"
---
# <a name="srealarray"></a><span data-ttu-id="c1dde-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="c1dde-103">SRealArray</span></span>

  
  
<span data-ttu-id="c1dde-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1dde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1dde-105">PT_MV_R4 の種類のプロパティを説明するために使用される浮動小数点値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c1dde-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1dde-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c1dde-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1dde-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1dde-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="c1dde-108">Members</span><span class="sxs-lookup"><span data-stu-id="c1dde-108">Members</span></span>

 <span data-ttu-id="c1dde-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="c1dde-109">**cValues**</span></span>
  
> <span data-ttu-id="c1dde-110">**Lpflt**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="c1dde-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="c1dde-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="c1dde-111">**lpflt**</span></span>
  
> <span data-ttu-id="c1dde-112">Float 値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1dde-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1dde-113">注釈</span><span class="sxs-lookup"><span data-stu-id="c1dde-113">Remarks</span></span>

<span data-ttu-id="c1dde-114">PT_MV_R4 プロパティのデータ型の詳細については、[プロパティの型](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1dde-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1dde-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1dde-115">See also</span></span>



[<span data-ttu-id="c1dde-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c1dde-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c1dde-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="c1dde-117">MAPI Structures</span></span>](mapi-structures.md)

