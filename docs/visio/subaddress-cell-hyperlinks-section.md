---
title: '[SubAddress] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
ms.localizationpriority: medium
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: リンク先のターゲット図面内での位置を指定します。
ms.openlocfilehash: cd3c69e932c393c463b9aa4ee1a0ebff1817d45e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569924"
---
# <a name="subaddress-cell-hyperlinks-section"></a>[SubAddress] セル ([Hyperlinks] セクション)

リンク先のターゲット図面内での位置を指定します。
  
## <a name="remarks"></a>注釈

たとえば、[アドレス] セルが "Drawing1.vsdx" の場合、[SubAddress] セルは"Page-3" などのページ名を指定できます。 [アドレス] セルが Microsoft Excel ファイル "Samples.xlsx" の場合、このセルの値は、ワークシート内のワークシートまたは範囲 ("Worksheet Functions" や "Sheet1!A1:D10". [アドレス] セルが ""の場合、このセルの値は、"ソリューション" など、ドキュメント内の名前付きアンカー https://www.microsoft.com/office/ になります。
  
このセルの値は、[**ハイパーリンク**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**リンク**] グループで、[**ハイパーリンク**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SubAddress] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *name*  .SubAddress where Hyperlink  *.name is the row*  name  <br/> |
   
プログラムからインデックスによって **[SubAddress]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visHLinkSubAddress** <br/> |
   

