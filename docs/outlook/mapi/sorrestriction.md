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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 054625601b496a8ec8f7745aa4cbc4715eed81a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585060"
---
# <a name="sorrestriction"></a><span data-ttu-id="ab6ab-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="ab6ab-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="ab6ab-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab6ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab6ab-105">制約を論理**OR**演算を適用するために使用する**か**制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="ab6ab-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab6ab-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ab6ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab6ab-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab6ab-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="ab6ab-108">Members</span><span class="sxs-lookup"><span data-stu-id="ab6ab-108">Members</span></span>

 <span data-ttu-id="ab6ab-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="ab6ab-109">**cRes**</span></span>
  
> <span data-ttu-id="ab6ab-110">**LpRes**メンバーが指す配列内の構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="ab6ab-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="ab6ab-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="ab6ab-111">**lpRes**</span></span>
  
> <span data-ttu-id="ab6ab-112">論理**OR**演算を使用して参加している制限を表す[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab6ab-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ab6ab-113">注釈</span><span class="sxs-lookup"><span data-stu-id="ab6ab-113">Remarks</span></span>

<span data-ttu-id="ab6ab-114">**SOrRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab6ab-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab6ab-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab6ab-115">See also</span></span>



[<span data-ttu-id="ab6ab-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="ab6ab-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="ab6ab-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ab6ab-117">MAPI Structures</span></span>](mapi-structures.md)

