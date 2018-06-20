---
title: '[Snap] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: レイヤーに割り当てられた図形に他の図形をスナップできるかどうかを指定します。レイヤーに割り当てられた図形に他の図形をスナップすることはできますが、他の図形にレイヤーに割り当てられた図形をスナップすることはできません。
ms.openlocfilehash: 7fc684afb67d0454ea5907c08f4f7644d97c7f74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806514"
---
# <a name="snap-cell-layers-section"></a>[Snap] セル ([Layers] セクション)

レイヤーに割り当てられた図形に他の図形をスナップできるかどうかを指定します。レイヤーに割り当てられた図形に他の図形をスナップすることはできますが、他の図形にレイヤーに割り当てられた図形をスナップすることはできません。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |レイヤー上の図形に他の図形をスナップできます。  <br/> |
|FALSE  <br/> |レイヤー上の図形に他の図形をスナップできません。  <br/> |
   
## <a name="remarks"></a>注釈

**[レイヤー プロパティ**] ダイアログ ボックスで、[**スナップ**] オプションを使用してこのセルの値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって snap] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Snap [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [snap] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visLayerSnap** <br/> |
   

