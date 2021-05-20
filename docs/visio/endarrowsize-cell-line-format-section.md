---
title: '[EndArrowSize] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251630
localization_priority: Normal
ms.assetid: e2ecf7c0-a0e9-951f-676a-8e5857bb6544
description: 線の終端にある矢印のサイズを指定します。
ms.openlocfilehash: 768a2b2adb05248049377eaee07194cdb89ed810
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438079"
---
# <a name="endarrowsize-cell-line-format-section"></a>[EndArrowSize] セル ([Line Format] セクション)

線の終端にある矢印のサイズを指定します。
  
|**値**|**[サイズ]**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |極小  <br/> |**visArrowSizeVerySmall** <br/> |
|1  <br/> |小  <br/> |**visArrowSizeSmall** <br/> |
|2  <br/> |中  <br/> |**visArrowSizeMedium** <br/> |
|3  <br/> |大  <br/> |**visArrowSizeLarge** <br/> |
|4  <br/> |特大  <br/> |**visArrowSizeVeryLarge** <br/> |
|5  <br/> |ジャンボ  <br/> |**visArrowSizeJumbo** <br/> |
|6  <br/> |Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>注釈

この値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**矢印**]、[**その他の矢印**] の順にクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EndArrowSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |EndArrowSize  <br/> |
   
プログラムから、インデックスによって [EndArrowSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineEndArrowSize** <br/> |
   

