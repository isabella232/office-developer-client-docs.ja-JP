---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: 空き/予約済みブロックの空き/予約済みの状態の列挙です。
ms.openlocfilehash: 67d710f82856dc8ff4839c926018eef88d355f73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19799316"
---
# <a name="fbstatus"></a>FBStatus

空き/予約済みブロックの空き/予約済みの状態の列挙です。
  
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

## <a name="remarks"></a>注釈

時間帯の空き/予約済みの状態では、カレンダー上の表示方法を決定します。**空き**、**予定あり**、**仮承諾**、または**不在時の Office**です。 
  
## <a name="see-also"></a>関連項目

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

