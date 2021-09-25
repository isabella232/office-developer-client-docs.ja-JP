---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: 空き時間情報ブロックの空き時間情報の状態の列挙。
ms.openlocfilehash: 61ac90849e2a0d40b48281cb6f145fc5d997d545
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592803"
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

