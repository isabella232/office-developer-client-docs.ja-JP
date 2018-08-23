---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d277908d3ec96537f63511e4d50488a694696bd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581224"
---
# <a name="sapptimearray"></a><span data-ttu-id="a1300-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="a1300-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="a1300-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1300-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1300-105">時刻の値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a1300-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1300-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a1300-106">Header file:</span></span>  <br/> |<span data-ttu-id="a1300-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1300-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="a1300-108">Members</span><span class="sxs-lookup"><span data-stu-id="a1300-108">Members</span></span>

 <span data-ttu-id="a1300-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="a1300-109">**cValues**</span></span>
  
> <span data-ttu-id="a1300-110">**Lpat**のメンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="a1300-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="a1300-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="a1300-111">**lpat**</span></span>
  
> <span data-ttu-id="a1300-112">アプリケーションの時刻の値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1300-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a1300-113">注釈</span><span class="sxs-lookup"><span data-stu-id="a1300-113">Remarks</span></span>

<span data-ttu-id="a1300-114">**SAppTimeArray**構造体を使用して、PT_MV_APPTIME の種類のプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="a1300-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="a1300-115">PT_MV_APPTIME の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1300-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1300-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1300-116">See also</span></span>



[<span data-ttu-id="a1300-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="a1300-117">MAPI Structures</span></span>](mapi-structures.md)

