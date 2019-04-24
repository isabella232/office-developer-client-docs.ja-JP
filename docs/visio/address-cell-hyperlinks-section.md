---
title: '[Address] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: 移動先の URL アドレス、ファイル名、または UNC パスを指定します。
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338550"
---
# <a name="address-cell-hyperlinks-section"></a>[Address] セル ([Hyperlinks] セクション)

移動先の URL アドレス、ファイル名、または UNC パスを指定します。
  
Address を相対パスとして指定するには、[**プロパティ**] ダイアログボックスの [ **** **概要**] タブで、[**ファイル**] タブをクリックし、[**情報**] をクリックし、[* * Properties * *] をクリックします。をクリックし、[**プロパティの詳細**] をクリックします。 図面にベース パスが定義されていない場合は、図面のパスに基づいて移動先が決まります。 図面が保存されないと、ハイパーリンクは未定義になります。
  
## <a name="remarks"></a>解説

[Address] セルの値は [**ハイパーリンク**] ダイアログ ボックスでも設定できます (このダイアログ ボックスを表示するには、[**挿入**] タブで [**ハイパーリンク**] をクリックします)。 
  
プログラムから、インデックスによって [Address] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ハイパーリンク *名前*です。ハイパーリンクのアドレスを指定します。 *name*は、ハイパーリンク行の名前です。  <br/> |
   
別の数式または**CellsU**プロパティを使用してプログラムから、名前によって [Address] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**vishlinkaddress** <br/> |
   

