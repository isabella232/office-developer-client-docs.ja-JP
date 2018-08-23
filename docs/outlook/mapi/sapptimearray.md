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
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803794"
---
# <a name="sapptimearray"></a><span data-ttu-id="361c6-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="361c6-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="361c6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="361c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="361c6-105">時刻の値の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="361c6-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="361c6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="361c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="361c6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="361c6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="361c6-108">Members</span><span class="sxs-lookup"><span data-stu-id="361c6-108">Members</span></span>

 <span data-ttu-id="361c6-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="361c6-109">**cValues**</span></span>
  
> <span data-ttu-id="361c6-110">**Lpat**のメンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="361c6-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="361c6-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="361c6-111">**lpat**</span></span>
  
> <span data-ttu-id="361c6-112">アプリケーションの時刻の値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="361c6-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="361c6-113">注釈</span><span class="sxs-lookup"><span data-stu-id="361c6-113">Remarks</span></span>

<span data-ttu-id="361c6-114">**SAppTimeArray**構造体を使用して、PT_MV_APPTIME の種類のプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="361c6-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="361c6-115">PT_MV_APPTIME の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="361c6-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="361c6-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="361c6-116">See also</span></span>



[<span data-ttu-id="361c6-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="361c6-117">MAPI Structures</span></span>](mapi-structures.md)

