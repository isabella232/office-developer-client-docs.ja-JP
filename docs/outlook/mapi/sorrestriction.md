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
# <a name="sorrestriction"></a><span data-ttu-id="24e09-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="24e09-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="24e09-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24e09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24e09-105">制限に論理**or**演算を適用するために使用される**or**制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="24e09-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24e09-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="24e09-106">Header file:</span></span>  <br/> |<span data-ttu-id="24e09-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24e09-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="24e09-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="24e09-108">Members</span></span>

 <span data-ttu-id="24e09-109">**cres**</span><span class="sxs-lookup"><span data-stu-id="24e09-109">**cRes**</span></span>
  
> <span data-ttu-id="24e09-110">**lpres**メンバによって参照されている配列内の構造体の数。</span><span class="sxs-lookup"><span data-stu-id="24e09-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="24e09-111">**lpres**</span><span class="sxs-lookup"><span data-stu-id="24e09-111">**lpRes**</span></span>
  
> <span data-ttu-id="24e09-112">論理**OR**演算を使用して結合する制限について説明する[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="24e09-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="24e09-113">注釈</span><span class="sxs-lookup"><span data-stu-id="24e09-113">Remarks</span></span>

<span data-ttu-id="24e09-114">**sorrestriction**構造の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24e09-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="24e09-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="24e09-115">See also</span></span>



[<span data-ttu-id="24e09-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="24e09-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="24e09-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="24e09-117">MAPI Structures</span></span>](mapi-structures.md)

