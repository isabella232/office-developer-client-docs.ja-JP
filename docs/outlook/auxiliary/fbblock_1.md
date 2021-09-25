---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: データの空き時間情報ブロックを定義します。 これは、予定または会議出席依頼で表される予定表のアイテムです。
ms.openlocfilehash: 5cf556e4df99801a56857d55c43b008f4071f714
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557324"
---
# <a name="fbblock_1"></a>FBBlock_1

データの空き時間情報ブロックを定義します。 これは、予定または会議出席依頼で表される予定表のアイテムです。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a>メンバー

_m_tmStart_
  
> ブロックの開始時刻を相対時間で表します。 詳細については、「相対時間を [使用して空き時間情報にアクセスする」を参照してください](how-to-use-relative-time-to-access-free-busy-data.md)。
    
_m_tmEnd_
  
> ブロックの終了時刻を相対時間で表します。
    
_m_fbStatus_
  
> このブロックの空き時間情報の状態 (ユーザーが m_tmStart から m_tmEnd の間の期間中に、ユーザーが会社外、ビジー状態、仮の状態、または空き時間情報であるかどうかを _示します_。
    
## <a name="see-also"></a>関連項目

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)

