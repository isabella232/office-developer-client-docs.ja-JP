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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406781"
---
# <a name="sdatetimearray"></a><span data-ttu-id="6b7c1-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="6b7c1-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="6b7c1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b7c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b7c1-105">PT_MV_SYSTIME 型のプロパティを記述するために使用される時間の値の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="6b7c1-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6b7c1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6b7c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b7c1-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b7c1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="6b7c1-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="6b7c1-108">Members</span></span>

 <span data-ttu-id="6b7c1-109">**cvalues**</span><span class="sxs-lookup"><span data-stu-id="6b7c1-109">**cValues**</span></span>
  
> <span data-ttu-id="6b7c1-110">**lpft**メンバーが指す配列内の値の数。</span><span class="sxs-lookup"><span data-stu-id="6b7c1-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="6b7c1-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="6b7c1-111">**lpft**</span></span>
  
> <span data-ttu-id="6b7c1-112">時刻の値を含む[FILETIME](filetime.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b7c1-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b7c1-113">注釈</span><span class="sxs-lookup"><span data-stu-id="6b7c1-113">Remarks</span></span>

<span data-ttu-id="6b7c1-114">PT_MV_SYSTIME の詳細については、「[プロパティの種類の一覧](property-types.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7c1-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b7c1-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b7c1-115">See also</span></span>



[<span data-ttu-id="6b7c1-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="6b7c1-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="6b7c1-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6b7c1-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6b7c1-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="6b7c1-118">MAPI Structures</span></span>](mapi-structures.md)

