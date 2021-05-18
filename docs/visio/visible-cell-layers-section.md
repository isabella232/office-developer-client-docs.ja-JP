---
title: '[Visible] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: レイヤーに属している図形が図面ページに表示されるかどうかを指定します。
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405451"
---
# <a name="visible-cell-layers-section"></a>[Visible] セル ([Layers] セクション)

レイヤーに属している図形が図面ページに表示されるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形は表示されます。  <br/> |
|FALSE  <br/> |図形は表示されません。  <br/> |
   
## <a name="remarks"></a>注釈

このセルは、[レイヤープロパティ] ダイアログ ボックスの [表示]オプションに対応します([ホーム] タブの [編集] グループで、[レイヤー] をクリックし、[レイヤー プロパティ] を **クリックします**)。  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Visible] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Visible[ *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Visible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visLayerVisible** <br/> |
   

