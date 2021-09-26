---
title: '[ObjectKind] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
ms.localizationpriority: medium
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: テキスト フィールドの種類を示します。
ms.openlocfilehash: 0186c510ed47550f5c1194b84dbe7eec6ee4c539
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627829"
---
# <a name="objectkind-cell-text-fields-section"></a>[ObjectKind] セル ([Text Fields] セクション)

テキスト フィールドの種類を示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | Standard  <br/> |**visTFOKStandard** <br/> |
| 1  <br/> |縦中横  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>注釈

テキスト フィールドは、次のいずれかの種類に該当します。
  
- 標準 : フィールド カテゴリ別に挿入された横書きテキストであることを示すフィールドです。
    
- 縦中横 : 縦書きテキストの内部に設定された横書きテキストであることを示すフィールドです。
    
別の数式または **CellsU** を使用したプログラムから、名前によって [ObjectKind] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Fields.ObjectKind[  *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [ObjectKind] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visFieldObjectKind** <br/> |
   

