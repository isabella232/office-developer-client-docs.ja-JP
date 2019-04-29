---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: 空き時間ブロックの空き時間状態の列挙体。
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424092"
---
# <a name="fbstatus"></a><span data-ttu-id="f4093-103">FBStatus</span><span class="sxs-lookup"><span data-stu-id="f4093-103">FBStatus</span></span>

<span data-ttu-id="f4093-104">空き時間ブロックの空き時間状態の列挙体。</span><span class="sxs-lookup"><span data-stu-id="f4093-104">An enumeration for the free/busy status of free/busy blocks.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f4093-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f4093-105">Quick info</span></span>

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a><span data-ttu-id="f4093-106">注釈</span><span class="sxs-lookup"><span data-stu-id="f4093-106">Remarks</span></span>

<span data-ttu-id="f4093-107">時間ブロックの空き時間状態によって、予定表での表示方法が決定されます。**空き**時間、**取り込み中**、 \*\*\*\*\*\*仮承諾\*\*、または外出中。</span><span class="sxs-lookup"><span data-stu-id="f4093-107">The free/busy status of a block of time determines how it is displayed on a calendar: **Free**, **Busy**, **Tentative**, or **Out of Office**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4093-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4093-108">See also</span></span>

- [<span data-ttu-id="f4093-109">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="f4093-109">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="f4093-110">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="f4093-110">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)

