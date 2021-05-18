---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: データの空き時間情報ブロックを定義します。 これは、予定または会議出席依頼で表される予定表のアイテムです。
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413200"
---
# <a name="fbblock_1"></a><span data-ttu-id="9721c-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="9721c-104">FBBlock_1</span></span>

<span data-ttu-id="9721c-105">データの空き時間情報ブロックを定義します。</span><span class="sxs-lookup"><span data-stu-id="9721c-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="9721c-106">これは、予定または会議出席依頼で表される予定表のアイテムです。</span><span class="sxs-lookup"><span data-stu-id="9721c-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9721c-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9721c-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="9721c-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="9721c-108">Members</span></span>

<span data-ttu-id="9721c-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="9721c-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="9721c-110">ブロックの開始時刻を相対時間で表します。</span><span class="sxs-lookup"><span data-stu-id="9721c-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="9721c-111">詳細については、「相対時間を [使用して空き時間情報にアクセスする」を参照してください](how-to-use-relative-time-to-access-free-busy-data.md)。</span><span class="sxs-lookup"><span data-stu-id="9721c-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="9721c-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="9721c-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="9721c-113">ブロックの終了時刻を相対時間で表します。</span><span class="sxs-lookup"><span data-stu-id="9721c-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="9721c-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="9721c-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="9721c-115">このブロックの空き時間情報の状態 (ユーザーが m_tmStart から m_tmEnd の間の期間中に、ユーザーが会社外、ビジー状態、仮の状態、または空き時間情報であるかどうかを _示します_。</span><span class="sxs-lookup"><span data-stu-id="9721c-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9721c-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="9721c-116">See also</span></span>

- [<span data-ttu-id="9721c-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="9721c-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="9721c-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="9721c-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="9721c-119">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="9721c-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

