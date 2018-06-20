---
title: '[ObjectKind] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: テキスト フィールドの種類を示します。
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805929"
---
# <a name="objectkind-cell-text-fields-section"></a>[ObjectKind] セル ([Text Fields] セクション)

テキスト フィールドの種類を示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 標準  <br/> |**visTFOKStandard** <br/> |
| 1  <br/> |縦中横  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>備考

テキスト フィールドは、次のいずれかの種類に該当します。
  
- 標準 : フィールド カテゴリ別に挿入された横書きテキストであることを示すフィールドです。
    
- 縦中横 : 縦書きテキストの内部に設定された横書きテキストであることを示すフィールドです。
    
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ObjectKind] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Fields.ObjectKind [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [ObjectKind] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visFieldObjectKind** <br/> |
   

