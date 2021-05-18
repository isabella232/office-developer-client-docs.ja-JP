---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: 夏時間の開始時期と、そのタイム ゾーン ルールが最初に有効な年に関するタイム ゾーン ルールの情報を指定します。
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328617"
---
# <a name="tzrule"></a>TZRULE

夏時間の開始時期と、そのタイム ゾーン ルールが最初に有効な年に関するタイム ゾーン ルールの情報を指定します。 
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a>メンバー

_wFlags_
  
> このメンバーに設定されたフラグは、このタイム ゾーン ルールの特定の詳細を識別します。 可能なフラグは次のとおりです。
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** —ルールを現在使用するルールとして識別します。 有効なルールとしてマークできるルールは 1 つのみです。 その他のすべてのルールは、比較のみを目的とします。 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** —定期的な会議では [、PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)のルールと一致するルールとしてルールを識別します。 これは **、PidLidTimeZoneStruct** が従来のクライアントによって大幅に変更されたかどうかを検出するために使用できます。 
    
_stStart_
  
> タイム ゾーン ルールが開始した協定世界時 (UTC) の時刻。
    
_TZReg_
  
> タイム ゾーン ルールのタイム ゾーン情報。
    
## <a name="remarks"></a>注釈

この構造は、タイム ゾーン ルールがいつ有効なのかを示す追加情報を提供することで [、TZREG](tzreg.md) を強化します。 
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

