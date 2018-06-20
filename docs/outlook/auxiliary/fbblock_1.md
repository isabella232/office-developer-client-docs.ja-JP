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
# <a name="fbblock1"></a>FBBlock_1

空き時間情報データ ブロックを定義します。 これは、予定または会議出席依頼で表される、予定表のアイテムです。
  
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
  
> ブロックの開始時刻は、相対時間で表されます。 詳細については、[空き時間情報データにアクセスするのには相対的な時間の使用](how-to-use-relative-time-to-access-free-busy-data.md)を参照してください。
    
_m_tmEnd_
  
> 相対時間で表現される、ブロックの終了時間です。
    
_m_fbStatus_
  
> ユーザーを示すかどうか、不在時の使用中、仮承諾、または無料で_m_tmStart_と_m_tmEnd_の間の期間中に、このブロックの空き/予約済みの状態です。
    
## <a name="see-also"></a>関連項目

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [空き時間情報データにアクセスする相対時間を使用します。](how-to-use-relative-time-to-access-free-busy-data.md)

