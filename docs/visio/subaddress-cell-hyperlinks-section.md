---
title: '[SubAddress] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: リンク先のターゲット図面内での位置を指定します。
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395267"
---
# <a name="subaddress-cell-hyperlinks-section"></a>[SubAddress] セル ([ハイパーリンク] セクション)

リンク先のターゲット図面内での位置を指定します。
  
## <a name="remarks"></a>注釈

たとえば、アドレスのセルが"Drawing1.vsdx"の場合は、サブアドレスのセルは「ページ 3」などのページ名を指定できます。 します ワークシートまたは範囲を「ワークシート関数」や「Sheet1 など、ワークシート内セルの値は、アドレスのセルが Excel のファイル"Samples.xlsx"の場合は、!範囲 A1: D10"です。 場合は、[Address] セルは、"https://www.microsoft.com/office/"、このセルの値は「ソリューション」など、ドキュメント内で名前付きアンカーをすることができます。
  
このセルの値は、[**ハイパーリンク**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**リンク**] グループで、[**ハイパーリンク**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SubAddress] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *名*です。サブアドレスのハイパーリンクの *.name*と行の名前があります。  <br/> |
   
プログラムから、インデックスによって [ **SubAddress** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visHLinkSubAddress** <br/> |
   

