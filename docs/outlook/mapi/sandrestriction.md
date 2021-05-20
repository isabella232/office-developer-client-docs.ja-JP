---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438884"
---
# <a name="sandrestriction"></a><span data-ttu-id="d45a3-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="d45a3-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="d45a3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d45a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d45a3-105">論理 AND 操作 **を使用** して制限のグループに参加するために使用される AND 制限について **説明** します。</span><span class="sxs-lookup"><span data-stu-id="d45a3-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d45a3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d45a3-106">Header file:</span></span>  <br/> |<span data-ttu-id="d45a3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d45a3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="d45a3-108">Members</span><span class="sxs-lookup"><span data-stu-id="d45a3-108">Members</span></span>

 <span data-ttu-id="d45a3-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="d45a3-109">**cRes**</span></span>
  
> <span data-ttu-id="d45a3-110">**lpRes** メンバーが指す配列内の検索制限の数。</span><span class="sxs-lookup"><span data-stu-id="d45a3-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="d45a3-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="d45a3-111">**lpRes**</span></span>
  
> <span data-ttu-id="d45a3-112">論理 **AND** 操作と組み合わせる [SRestriction](srestriction.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d45a3-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d45a3-113">注釈</span><span class="sxs-lookup"><span data-stu-id="d45a3-113">Remarks</span></span>

<span data-ttu-id="d45a3-114">すべての子制限が TRUE に評価される場合 **、SAndRestriction** の結果は TRUE です。</span><span class="sxs-lookup"><span data-stu-id="d45a3-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="d45a3-115">子制限が FALSE と評価される場合は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="d45a3-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="d45a3-116">制限の種類、それらをビルドする方法、およびサンプル コードの説明については、「制限について [」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="d45a3-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d45a3-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="d45a3-117">See also</span></span>



[<span data-ttu-id="d45a3-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="d45a3-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="d45a3-119">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d45a3-119">MAPI Structures</span></span>](mapi-structures.md)

