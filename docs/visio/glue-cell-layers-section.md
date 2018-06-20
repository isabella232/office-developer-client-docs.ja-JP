---
title: '[Glue] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: レイヤーに属している図形が接着可能かどうかを指定します。
ms.openlocfilehash: 81a54bebaa8ca68a8fbc8853c69f88efb34bbdb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805471"
---
# <a name="glue-cell-layers-section"></a>[Glue] セル ([Layers] セクション)

レイヤーに属している図形が接着可能かどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |接着できます。  <br/> |
|FALSE  <br/> |接着できません。  <br/> |
   
## <a name="remarks"></a>注釈

このセルは、 **[レイヤー プロパティ**] ダイアログ ボックスで [**接着**] オプションに対応して ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Glue] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Glue [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Glue] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visLayerGlue** <br/> |
   

