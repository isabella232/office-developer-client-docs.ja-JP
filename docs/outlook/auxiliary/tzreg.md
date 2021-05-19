---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: 夏時間の開始時刻、標準時への戻り時間、夏時間シフトの時間数を定義します。
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419367"
---
# <a name="tzreg"></a>TZREG

夏時間の開始時刻、標準時への戻り時間、夏時間シフトの時間数を定義します。
  
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

## <a name="members"></a>メンバー

_lBias_
  
> グリニッジ標準時 (GMT) からのオフセット。
    
_lStandardBias_
  
> 標準時のバイアスからのオフセット。
    
_lDaylightBias_
  
> 夏時間中のバイアスからのオフセット。
    
_stStandardDate_
  
> 標準時刻に切り替える時間。
    
_stDaylightDate_
  
> 夏時間に切り替える時間。
    
## <a name="remarks"></a>注釈

この構造は、TIME_ZONE_INFORMATION に **似ています**。 これは、従来のクライアントが定期的な会議のタイム ゾーン情報を格納するために使用する構造です。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

