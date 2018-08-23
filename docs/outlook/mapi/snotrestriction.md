---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575064"
---
# <a name="snotrestriction"></a><span data-ttu-id="a6209-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="a6209-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="a6209-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6209-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6209-105">**しない**制限、制約を論理**NOT**演算を適用するために使用について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6209-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6209-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a6209-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6209-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6209-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="a6209-108">Members</span><span class="sxs-lookup"><span data-stu-id="a6209-108">Members</span></span>

 <span data-ttu-id="a6209-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="a6209-109">**ulReserved**</span></span>
  
> <span data-ttu-id="a6209-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a6209-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a6209-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="a6209-111">**lpRes**</span></span>
  
> <span data-ttu-id="a6209-112">論理**NOT**演算子に参加している制限を記述する[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a6209-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a6209-113">注釈</span><span class="sxs-lookup"><span data-stu-id="a6209-113">Remarks</span></span>

<span data-ttu-id="a6209-114">**SNotRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6209-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6209-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6209-115">See also</span></span>



[<span data-ttu-id="a6209-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a6209-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="a6209-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="a6209-117">MAPI Structures</span></span>](mapi-structures.md)

