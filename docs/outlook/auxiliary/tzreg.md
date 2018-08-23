---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: 時刻が夏時間の開始時、標準時間へのリターンが発生すると、および夏時間のシフトは、時間数を定義します。
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799594"
---
# <a name="tzreg"></a>TZREG

時刻が夏時間の開始時、標準時間へのリターンが発生すると、および夏時間のシフトは、時間数を定義します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a>Members

_lBias_
  
> グリニッジ標準時 (GMT) からのオフセット。
    
_lStandardBias_
  
> 標準時間の間のバイアスからのオフセット。
    
_lDaylightBias_
  
> サマータイム期間中のバイアスからのオフセット。
    
_stStandardDate_
  
> (標準時) に切り替えるには時間です。
    
_stDaylightDate_
  
> 夏時間への切り替えにかかる時間です。
    
## <a name="remarks"></a>注釈

この構造体は、 **TIME_ZONE_INFORMATION**に似ています。 これは、定期的なミーティングのタイム ゾーン情報を保存するのにはレガシ クライアントで使用する構造体です。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

