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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803966"
---
# <a name="snotrestriction"></a><span data-ttu-id="87959-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="87959-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="87959-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87959-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87959-105">**しない**制限、制約を論理**NOT**演算を適用するために使用について説明します。</span><span class="sxs-lookup"><span data-stu-id="87959-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87959-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="87959-106">Header file:</span></span>  <br/> |<span data-ttu-id="87959-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87959-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="87959-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="87959-108">Members</span></span>

 <span data-ttu-id="87959-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="87959-109">**ulReserved**</span></span>
  
> <span data-ttu-id="87959-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="87959-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="87959-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="87959-111">**lpRes**</span></span>
  
> <span data-ttu-id="87959-112">論理**NOT**演算子に参加している制限を記述する[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="87959-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="87959-113">備考</span><span class="sxs-lookup"><span data-stu-id="87959-113">Remarks</span></span>

<span data-ttu-id="87959-114">**SNotRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87959-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87959-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="87959-115">See also</span></span>



[<span data-ttu-id="87959-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="87959-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="87959-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="87959-117">MAPI Structures</span></span>](mapi-structures.md)

