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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803812"
---
# <a name="sandrestriction"></a><span data-ttu-id="1bd67-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="1bd67-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="1bd67-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1bd67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1bd67-105">論理**AND**演算を使用して制限のグループに参加するために使用、**および**制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="1bd67-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bd67-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1bd67-106">Header file:</span></span>  <br/> |<span data-ttu-id="1bd67-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1bd67-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="1bd67-108">Members</span><span class="sxs-lookup"><span data-stu-id="1bd67-108">Members</span></span>

 <span data-ttu-id="1bd67-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="1bd67-109">**cRes**</span></span>
  
> <span data-ttu-id="1bd67-110">**LpRes**メンバーが指す配列内の検索制限の数です。</span><span class="sxs-lookup"><span data-stu-id="1bd67-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="1bd67-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="1bd67-111">**lpRes**</span></span>
  
> <span data-ttu-id="1bd67-112">論理**AND**演算では、結合されている[SRestriction](srestriction.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1bd67-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1bd67-113">注釈</span><span class="sxs-lookup"><span data-stu-id="1bd67-113">Remarks</span></span>

<span data-ttu-id="1bd67-114">**SAndRestriction**の結果は、その子のすべての制約が TRUE と評価される場合は TRUE です。</span><span class="sxs-lookup"><span data-stu-id="1bd67-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="1bd67-115">子の制限は、FALSE に評価された場合は FALSE になります。</span><span class="sxs-lookup"><span data-stu-id="1bd67-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="1bd67-116">制限の種類の説明については、ビルドし、および方法のサンプル コード[についての制限](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1bd67-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1bd67-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="1bd67-117">See also</span></span>



[<span data-ttu-id="1bd67-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="1bd67-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="1bd67-119">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="1bd67-119">MAPI Structures</span></span>](mapi-structures.md)

