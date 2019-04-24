---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: 夏時間のすべての過去、現在、および今後のタイムゾーンシフトルールを含むタイムゾーン全体を表します。
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328295"
---
# <a name="tzdefinition"></a>TZDEFINITION

夏時間のすべての過去、現在、および今後のタイムゾーンシフトルールを含むタイムゾーン全体を表します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a>メンバー

_wflags_
  
> Windows レジストリのタイムゾーンを表すキー名が有効であることを示します。 各タイムゾーンは常にキー名によって識別される必要があるため、このメンバーの値は常に**TZDEFINITION_FLAG_VALID_KEYNAME**にする必要があります。
    
_pwszKeyName_
  
> Windows レジストリ内のこのタイムゾーンのキーの名前。 この名前はローカライズしないでください。 これは、windows Software Development Kit (SDK) ヘッダーファイル windows で定義されている**MAX_PATH**の最大サイズを持ちます。 
    
_crules しくみ_
  
> この定義のタイムゾーンルールの数。 ルールの最大数は**TZ_MAX_RULES**です。 
    
_rgrules_
  
> シフトが発生するタイミングを記述するルールの配列です。
    
## <a name="remarks"></a>解説

*rgrules* 、少なくとも1つのルールが必要です。 [ *rgrules*の最初のルールは、最初のルールの*ststart*に関係なく、2番目のルールが開始されるまで使用するルールと見なされます。 
  
ルールは、最も古いものから [最新] に順に並べ替える必要があります。 ルール間に重複が許可されていないため、新しいルールが開始される前のルールが終了したと見なされます。
  
## <a name="see-also"></a>関連項目

- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

