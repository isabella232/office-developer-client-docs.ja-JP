---
title: '[Active] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
ms.localizationpriority: medium
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: レイヤーがアクティブであるかどうかを指定します。事前にレイヤーを割り当てられていない図形は、図面ページにドラッグしたときにアクティブになっているレイヤーに割り当てられます。
ms.openlocfilehash: bf300a911084cdd05e270bb3e960934d9a4e0e4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616048"
---
# <a name="active-cell-layers-section"></a>[Active] セル ([Layers] セクション)

レイヤーがアクティブであるかどうかを指定します。事前にレイヤーを割り当てられていない図形は、図面ページにドラッグしたときにアクティブになっているレイヤーに割り当てられます。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |レイヤーはアクティブです。  <br/> |
|FALSE  <br/> |レイヤーはアクティブではありません。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**レイヤー プロパティ**] ダイアログ ボックスの [**アクティブ**] の設定に対応しています (このダイアログ ボックスを開くには、[**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックして、[**レイヤー プロパティ**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Active] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Active[ *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Active] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visLayerActive** <br/> |
   

