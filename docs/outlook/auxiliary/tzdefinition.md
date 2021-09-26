---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: 夏時間のすべての履歴、現在、および将来のタイム ゾーン シフト ルールを含む、タイム ゾーン全体を表します。
ms.openlocfilehash: 845d2cb2195eb6736fe03f0b66e5110d692538ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631133"
---
# <a name="tzdefinition"></a>TZDEFINITION

夏時間のすべての履歴、現在、および将来のタイム ゾーン シフト ルールを含む、タイム ゾーン全体を表します。
  
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

_wFlags_
  
> レジストリ内のタイム ゾーンを表すキー名が有効Windows示します。 各タイム ゾーンは常にキー名で識別される必要があるから、このメンバーは常に値を持つ必要 **TZDEFINITION_FLAG_VALID_KEYNAME。**
    
_pwszKeyName_
  
> レジストリ内のこのタイム ゾーンのキー Windowsします。 この名前はローカライズする必要があります。 ソフトウェア開発キット (SDK) ヘッダー MAX_PATH windows.h で定義されている Windowsの最大サイズを持っています。  
    
_cRules_
  
> この定義のタイム ゾーン ルールの数。 ルールの最大数は次 **TZ_MAX_RULES。** 
    
_rgRules_
  
> シフトが発生する時間を表すルールの配列。
    
## <a name="remarks"></a>注釈

rgRules には少なくとも  *1 つのルールが必要です*  。 *rgRules* の最初のルールは、最初のルールの *stStart* に関係なく、2 番目のルールが開始されるまで使用するルールと見なされます。 
  
ルールは、最も古いルールから最新の順に並べ替える必要があります。 ルール間に重複は許可されません。そのため、以前のルールは新しいルールの開始時に終了すると見なされます。
  
## <a name="see-also"></a>関連項目

- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

