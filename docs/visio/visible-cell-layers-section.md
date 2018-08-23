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
ms.openlocfilehash: 9a025403b1f5b46d2f439805a15954eaeeab2686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806763"
---
# <a name="visible-cell-layers-section"></a>[Visible] セル ([レイヤー] セクション)

レイヤーに属している図形が図面ページに表示されるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形は表示されます。  <br/> |
|FALSE  <br/> |図形は表示されません。  <br/> |
   
## <a name="remarks"></a>注釈

このセルは、[**レイヤー プロパティ**] ダイアログ ボックスの**表示**オプションに対応して ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Visible] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Visible [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Visible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visLayerVisible** <br/> |
   

