---
title: '[Description] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: ハイパーリンクの説明文を表示します。
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360243"
---
# <a name="description-cell-hyperlinks-section"></a>[Description] セル ([Hyperlinks] セクション)

ハイパーリンクの説明文を表示します。 
  
## <a name="remarks"></a>解説

このセルを使用して、ハイパーリンクに関するコメントを保存します。たとえば、「価格 web サイトへのリンク」とします。
  
このセルの値は、[**ハイパーリンク**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**ハイパーリンク**] をクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Description] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *名前*です。ハイパーリンクの説明。  *name*は、ハイパーリンク行の名前です。  <br/> |
   
プログラムから、インデックスによって [Description] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**vishlinkdescription** <br/> |
   

