---
title: '[Address] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
ms.localizationpriority: medium
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: 移動先の URL アドレス、ファイル名、または UNC パスを指定します。
ms.openlocfilehash: ef893335b25fb400cbfc1f153a3fcdcd7a66be02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578292"
---
# <a name="address-cell-hyperlinks-section"></a>[Address] セル ([Hyperlinks] セクション)

移動先の URL アドレス、ファイル名、または UNC パスを指定します。
  
[プロパティ] ダイアログ ボックスの [概要] タブの [ハイパーリンク] ベース ボックスで、ドキュメントに対して定義されている基本パスに基づいて相対パスとしてAddress を指定できます ([ファイル] タブをクリックし、[情報] をクリックし、[** プロパティ **] をクリックし、[高度なプロパティ] をクリックします)。   図面にベース パスが定義されていない場合は、図面のパスに基づいて移動先が決まります。 図面が保存されないと、ハイパーリンクは未定義になります。
  
## <a name="remarks"></a>注釈

[Address] セルの値は [**ハイパーリンク**] ダイアログ ボックスでも設定できます (このダイアログ ボックスを表示するには、[**挿入**] タブで [**ハイパーリンク**] をクリックします)。 
  
プログラムから、インデックスによって [Address] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ハイパーリンク *name*  .ハイパーリンクのアドレス。 *name*  はハイパーリンク行の名前です  <br/> |
   
CellsU プロパティを使用して、別の数式またはプログラムから名前によって [アドレス] セルへの参照を **取得** するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visHLinkAddress** <br/> |
   

