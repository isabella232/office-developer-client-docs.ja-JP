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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426654"
---
# <a name="snotrestriction"></a><span data-ttu-id="685f6-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="685f6-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="685f6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="685f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="685f6-105">制限に制限を適用するのでは**なく**、制限に対して論理**not**演算を適用する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="685f6-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="685f6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="685f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="685f6-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="685f6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="685f6-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="685f6-108">Members</span></span>

 <span data-ttu-id="685f6-109">**ulreserved**</span><span class="sxs-lookup"><span data-stu-id="685f6-109">**ulReserved**</span></span>
  
> <span data-ttu-id="685f6-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="685f6-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="685f6-111">**lpres**</span><span class="sxs-lookup"><span data-stu-id="685f6-111">**lpRes**</span></span>
  
> <span data-ttu-id="685f6-112">論理**not**演算子に結合する制限を説明する[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="685f6-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="685f6-113">注釈</span><span class="sxs-lookup"><span data-stu-id="685f6-113">Remarks</span></span>

<span data-ttu-id="685f6-114">**snotrestriction**構造の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="685f6-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="685f6-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="685f6-115">See also</span></span>



[<span data-ttu-id="685f6-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="685f6-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="685f6-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="685f6-117">MAPI Structures</span></span>](mapi-structures.md)

