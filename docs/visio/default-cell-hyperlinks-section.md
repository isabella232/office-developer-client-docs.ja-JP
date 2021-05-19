---
title: '[Default] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: 図形またはページの既定のハイパーリンクを指定します。既定のハイパーリンクを設定するには、このセルの値を TRUE に設定します。
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434355"
---
# <a name="default-cell-hyperlinks-section"></a>[Default] セル ([Hyperlinks] セクション)

図形またはページの既定のハイパーリンクを指定します。既定のハイパーリンクを設定するには、このセルの値を TRUE に設定します。
  
## <a name="remarks"></a>注釈

既定のハイパーリンクは、図形をクリックして [**挿入**] タブの [**ハイパーリンク**] をクリックし、[**既定値**] をクリックすることで設定することもできます。既定のハイパーリンクは太字で表示されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Default] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ハイパーリンク *Name*  .[ハイパーリンク] の既定の場所。 *名前*  は行名です  <br/> |
   
プログラムから、インデックスによって [Default] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
|行インデックス:  <br/> |**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visHLinkDefault** <br/> |
   

