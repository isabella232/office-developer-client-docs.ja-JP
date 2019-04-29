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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413200"
---
# <a name="fbblock1"></a>FBBlock_1

データの空き時間情報のブロックを定義します。 これは、予定または会議出席依頼で表される予定表のアイテムです。
  
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
  
> 相対時間で表された、ブロックの開始時刻。 詳細については、「[相対時間を使用して空き時間情報データにアクセスする](how-to-use-relative-time-to-access-free-busy-data.md)」を参照してください。
    
_m_tmEnd_
  
> 相対時間で表された、ブロックの終了時刻。
    
_m_fbStatus_
  
> _m_tmStart_と_m_tmEnd_の間の期間中に、ユーザーが不在、取り込み中、仮承諾、または無料のいずれであるかを示す、このブロックの空き時間状態。
    
## <a name="see-also"></a>関連項目

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)

