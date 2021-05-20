---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437932"
---
# <a name="sorrestriction"></a><span data-ttu-id="df00f-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="df00f-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="df00f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df00f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df00f-105">論理 OR 操作 **を** 制限に適用するために使用される **OR** 制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="df00f-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df00f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="df00f-106">Header file:</span></span>  <br/> |<span data-ttu-id="df00f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df00f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="df00f-108">Members</span><span class="sxs-lookup"><span data-stu-id="df00f-108">Members</span></span>

 <span data-ttu-id="df00f-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="df00f-109">**cRes**</span></span>
  
> <span data-ttu-id="df00f-110">lpRes メンバーが指す配列内の **構造体の** 数。</span><span class="sxs-lookup"><span data-stu-id="df00f-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="df00f-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="df00f-111">**lpRes**</span></span>
  
> <span data-ttu-id="df00f-112">論理 OR 操作を使用して参加する制限を記述する [SRestriction](srestriction.md) 構造体 **への** ポインター。</span><span class="sxs-lookup"><span data-stu-id="df00f-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="df00f-113">注釈</span><span class="sxs-lookup"><span data-stu-id="df00f-113">Remarks</span></span>

<span data-ttu-id="df00f-114">**SOrRestriction** 構造の詳細については、「制限について [」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="df00f-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df00f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="df00f-115">See also</span></span>



[<span data-ttu-id="df00f-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="df00f-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="df00f-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="df00f-117">MAPI Structures</span></span>](mapi-structures.md)

