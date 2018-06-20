---
title: '[Active] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: レイヤーがアクティブであるかどうかを指定します。事前にレイヤーを割り当てられていない図形は、図面ページにドラッグしたときにアクティブになっているレイヤーに割り当てられます。
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804758"
---
# <a name="active-cell-layers-section"></a>[Active] セル ([Layers] セクション)

レイヤーがアクティブであるかどうかを指定します。事前にレイヤーを割り当てられていない図形は、図面ページにドラッグしたときにアクティブになっているレイヤーに割り当てられます。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |レイヤーは、アクティブです。  <br/> |
|FALSE  <br/> |レイヤーがアクティブではありません。  <br/> |
   
## <a name="remarks"></a>備考

このセルの値は、 **[レイヤー プロパティ**] ダイアログ ボックス内の**アクティブな**設定に対応する ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によってアクティブなセルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Active [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Active] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visLayerActive** <br/> |
   

