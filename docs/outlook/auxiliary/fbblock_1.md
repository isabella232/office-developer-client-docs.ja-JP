---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: データの空き時間情報のブロックを定義します。 これは、予定または会議出席依頼で表される予定表のアイテムです。
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317669"
---
# <a name="fbblock1"></a><span data-ttu-id="3558d-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="3558d-104">FBBlock_1</span></span>

<span data-ttu-id="3558d-105">データの空き時間情報のブロックを定義します。</span><span class="sxs-lookup"><span data-stu-id="3558d-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="3558d-106">これは、予定または会議出席依頼で表される予定表のアイテムです。</span><span class="sxs-lookup"><span data-stu-id="3558d-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3558d-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3558d-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="3558d-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="3558d-108">Members</span></span>

<span data-ttu-id="3558d-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="3558d-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="3558d-110">相対時間で表された、ブロックの開始時刻。</span><span class="sxs-lookup"><span data-stu-id="3558d-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="3558d-111">詳細については、「[相対時間を使用して空き時間情報データにアクセスする](how-to-use-relative-time-to-access-free-busy-data.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3558d-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="3558d-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="3558d-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="3558d-113">相対時間で表された、ブロックの終了時刻。</span><span class="sxs-lookup"><span data-stu-id="3558d-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="3558d-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="3558d-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="3558d-115">_m_tmStart_と_m_tmEnd_の間の期間中に、ユーザーが不在、取り込み中、仮承諾、または無料のいずれであるかを示す、このブロックの空き時間状態。</span><span class="sxs-lookup"><span data-stu-id="3558d-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3558d-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="3558d-116">See also</span></span>

- [<span data-ttu-id="3558d-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="3558d-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="3558d-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="3558d-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="3558d-119">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="3558d-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

