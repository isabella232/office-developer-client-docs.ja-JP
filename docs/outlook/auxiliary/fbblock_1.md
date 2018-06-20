---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: 空き時間情報データ ブロックを定義します。 これは、予定または会議出席依頼で表される、予定表のアイテムです。
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799305"
---
# <a name="fbblock1"></a><span data-ttu-id="45f52-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="45f52-104">FBBlock_1</span></span>

<span data-ttu-id="45f52-105">空き時間情報データ ブロックを定義します。</span><span class="sxs-lookup"><span data-stu-id="45f52-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="45f52-106">これは、予定または会議出席依頼で表される、予定表のアイテムです。</span><span class="sxs-lookup"><span data-stu-id="45f52-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="45f52-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="45f52-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="45f52-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="45f52-108">Members</span></span>

<span data-ttu-id="45f52-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="45f52-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="45f52-110">ブロックの開始時刻は、相対時間で表されます。</span><span class="sxs-lookup"><span data-stu-id="45f52-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="45f52-111">詳細については、[空き時間情報データにアクセスするのには相対的な時間の使用](how-to-use-relative-time-to-access-free-busy-data.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="45f52-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="45f52-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="45f52-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="45f52-113">相対時間で表現される、ブロックの終了時間です。</span><span class="sxs-lookup"><span data-stu-id="45f52-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="45f52-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="45f52-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="45f52-115">ユーザーを示すかどうか、不在時の使用中、仮承諾、または無料で_m_tmStart_と_m_tmEnd_の間の期間中に、このブロックの空き/予約済みの状態です。</span><span class="sxs-lookup"><span data-stu-id="45f52-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45f52-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="45f52-116">See also</span></span>

- [<span data-ttu-id="45f52-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="45f52-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="45f52-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="45f52-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="45f52-119">空き時間情報データにアクセスする相対時間を使用します。</span><span class="sxs-lookup"><span data-stu-id="45f52-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

