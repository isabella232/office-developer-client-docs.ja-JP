---
title: '[EndArrow] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: 線の最後の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805307"
---
# <a name="endarrow-cell-line-format-section"></a>[EndArrow] セル ([線の書式設定] セクション)

線の最後の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |矢印を付けません。  <br/> |
|1-45  <br/> |さまざまな矢印のスタイル。入力した値は、[**線**] ダイアログ ボックスでインデックスが付けられたエントリに対応します。  <br/> |
   
## <a name="remarks"></a>注釈

この値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**矢印**]、[**その他の矢印**] の順にクリックします)。 EndArrowSize] セルにある矢印のサイズが設定されています。
  
USE 関数を使用して、このセルにユーザー設定の線の端を指定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EndArrow] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[Endarrow]  <br/> |
   
プログラムから、インデックスによって [EndArrow] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineEndArrow** <br/> |
   

