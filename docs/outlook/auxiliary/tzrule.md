---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: 夏時間の開始時とでそのタイム ゾーン規則最初が発効した年のタイム ゾーン規則の情報を指定します。
ms.openlocfilehash: 77d56d238d959992bfadd2d8c143391ca6fa4d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799592"
---
# <a name="tzrule"></a>TZRULE

夏時間の開始時とでそのタイム ゾーン規則最初が発効した年のタイム ゾーン規則の情報を指定します。 
  
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
  
> このメンバーに設定されているフラグは、このタイム ゾーン規則の特定の詳細を確認します。 使用できるフラグは次のとおりです。
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** -現在使用すると、ルールを識別します。 1 つのルールは、有効なルールとしてマークできます。 他のすべての規則は、比較目的でのみです。 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG**などの定期的な会議は、 [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)のルールに一致するルールを識別します。 これになる場合は、新しいより包括的なプロパティに注意してください、古いバージョンのクライアントで**PidLidTimeZoneStruct**が大幅に変更されているかどうかを検出するために使用できます。 
    
_stStart_
  
> 世界協定時刻 (UTC) で、タイム ゾーン規則を開始した時刻。
    
_TZReg_
  
> タイム ゾーン規則のタイム ゾーン情報。
    
## <a name="remarks"></a>備考

この構造体は、タイム ゾーン規則が有効になるときを示す追加情報を提供することによって[TZREG](tzreg.md)を補強します。 
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

