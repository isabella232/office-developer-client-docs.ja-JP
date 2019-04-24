---
title: '[NewWindow] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: ハイパーリンクを新しいウィンドウで開くかどうかを指定します。
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342232"
---
# <a name="newwindow-cell-hyperlinks-section"></a>[NewWindow] セル ([Hyperlinks] セクション)

ハイパーリンクを新しいウィンドウで開くかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | リンクされたページ、ドキュメント、または web サイトを新しいウィンドウで開きます。  <br/> |
| FALSE  <br/> | 既定値です。ハイパーリンク用に新しいウィンドウを開きません。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NewWindow] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ハイパーリンク  *名前*です。NewWindow where ハイパーリンク。  *name*には、行の名前を指定します。  <br/> |
   
プログラムから、インデックスによって [NewWindow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* = ** 0、1、2、...  <br/> |
| セル インデックス:  <br/> |**vishlinknewwin** <br/> |
   

