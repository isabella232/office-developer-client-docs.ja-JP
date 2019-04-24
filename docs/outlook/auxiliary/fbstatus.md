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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319727"
---
# <a name="fbstatus"></a>FBStatus

空き時間ブロックの空き時間状態の列挙体。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a>解説

時間ブロックの空き時間状態によって、予定表での表示方法が決定されます。**空き**時間、**取り込み中**、 ******仮承諾**、または外出中。 
  
## <a name="see-also"></a>関連項目

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

