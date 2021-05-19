---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: 空き時間情報ブロックの空き時間情報の状態の列挙。
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424092"
---
# <a name="fbstatus"></a>FBStatus

空き時間情報ブロックの空き時間情報の状態の列挙。
  
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

時間のブロックの空き時間情報の状態は、予定表での表示方法を決定します。空き時間情報、空き時間情報、予定外 **Office。** 
  
## <a name="see-also"></a>関連項目

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)

