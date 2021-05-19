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
# <a name="snotrestriction"></a><span data-ttu-id="a64c0-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="a64c0-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="a64c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a64c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a64c0-105">論理 NOT **操作を** 制限に適用するために使用される **NOT** 制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="a64c0-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a64c0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a64c0-106">Header file:</span></span>  <br/> |<span data-ttu-id="a64c0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a64c0-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="a64c0-108">Members</span><span class="sxs-lookup"><span data-stu-id="a64c0-108">Members</span></span>

 <span data-ttu-id="a64c0-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="a64c0-109">**ulReserved**</span></span>
  
> <span data-ttu-id="a64c0-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a64c0-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a64c0-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="a64c0-111">**lpRes**</span></span>
  
> <span data-ttu-id="a64c0-112">論理 NOT 演算子に結合する制限を記述する [SRestriction](srestriction.md) 構造体 **への** ポインター。</span><span class="sxs-lookup"><span data-stu-id="a64c0-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a64c0-113">注釈</span><span class="sxs-lookup"><span data-stu-id="a64c0-113">Remarks</span></span>

<span data-ttu-id="a64c0-114">**SNotRestriction 構造の詳細については、「** 制限について [」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="a64c0-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a64c0-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a64c0-115">See also</span></span>



[<span data-ttu-id="a64c0-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a64c0-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="a64c0-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="a64c0-117">MAPI Structures</span></span>](mapi-structures.md)

