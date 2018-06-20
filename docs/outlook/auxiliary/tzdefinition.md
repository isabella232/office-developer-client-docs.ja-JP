---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: 夏時間のすべての過去、現在、および将来のタイム ゾーン シフトの規則を含む全体のタイム ゾーンを表します。
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799604"
---
# <a name="tzdefinition"></a>TZDEFINITION

夏時間のすべての過去、現在、および将来のタイム ゾーン シフトの規則を含む全体のタイム ゾーンを表します。
  
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
  
> Windows レジストリ内のタイム ゾーンを表すキー名が有効であることを示します。 各タイム ゾーンは、常に、キーの名前で識別する必要があります、ためこのメンバーは常に値を持つ**TZDEFINITION_FLAG_VALID_KEYNAME**。
    
_pwszKeyName_
  
> Windows レジストリには、このタイム ゾーンのキーの名前です。 この名前はローカライズされませんする必要があります。 **MAX_PATH**、Windows ソフトウェア開発キット (SDK) のヘッダー ファイル windows.h で定義されている最大サイズがあります。 
    
_cRules_
  
> この定義のタイム ゾーン規則の数です。 ルールの最大数は、 **TZ_MAX_RULES**です。 
    
_rgRules_
  
> シフトが発生する可能性を示す規則の配列。
    
## <a name="remarks"></a>備考

*RgRules*では、少なくとも 1 つのルールをする必要があります。 *RgRules*の最初のルールは、最初のルールの*stStart*に関係なく、2 番目のルールが開始されるまでに使用するルールを使用すると見なされます。 
  
規則は必要があります古いものから順に並べ替えられます。 以前の規則が新しいルールを起動したときに終了すると判断したため、ルール間の重複はありません。
  
## <a name="see-also"></a>関連項目

- [(Outlook エクスポート Api) 定数](constants-outlook-exported-apis.md)
- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

