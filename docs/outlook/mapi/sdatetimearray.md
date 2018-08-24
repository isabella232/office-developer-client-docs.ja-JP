---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: dc90f15835de35354a271d87a736366a4caf8dd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578781"
---
# <a name="sdatetimearray"></a><span data-ttu-id="058f5-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="058f5-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="058f5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="058f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="058f5-105">PT_MV_SYSTIME の種類のプロパティを説明するために使用する時刻の値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="058f5-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="058f5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="058f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="058f5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="058f5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="058f5-108">Members</span><span class="sxs-lookup"><span data-stu-id="058f5-108">Members</span></span>

 <span data-ttu-id="058f5-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="058f5-109">**cValues**</span></span>
  
> <span data-ttu-id="058f5-110">**Lpft**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="058f5-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="058f5-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="058f5-111">**lpft**</span></span>
  
> <span data-ttu-id="058f5-112">Time 値を格納する[FILETIME](filetime.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="058f5-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="058f5-113">注釈</span><span class="sxs-lookup"><span data-stu-id="058f5-113">Remarks</span></span>

<span data-ttu-id="058f5-114">PT_MV_SYSTIME の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="058f5-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="058f5-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="058f5-115">See also</span></span>



[<span data-ttu-id="058f5-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="058f5-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="058f5-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="058f5-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="058f5-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="058f5-118">MAPI Structures</span></span>](mapi-structures.md)

