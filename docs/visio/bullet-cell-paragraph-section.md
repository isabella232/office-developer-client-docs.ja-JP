---
title: '[Bullet] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
ms.localizationpriority: medium
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: 箇条書きのスタイルを指定します。
ms.openlocfilehash: b20b09cbf9785eb6bd988961f55097bd5fac34d7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554825"
---
# <a name="bullet-cell-paragraph-section"></a>[Bullet] セル ([Paragraph] セクション)

箇条書きのスタイルを指定します。
  
|**値**|**箇条書きスタイル**|
|:-----|:-----|
|0  <br/> |None  <br/> |
|1  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|3  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|4   <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|5  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|6   <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|7   <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
|行インデックス:  <br/> |**visRowParagraph**  +  *i* *=* 0, 1, 2, ...  <br/> |
|セル インデックス:  <br/> |**visBulletIndex** <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、図形を右クリックして [**書式**] をポイントし、[**テキスト**]、[**箇条書き**] の順にクリックして設定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Bullet] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Para.Bullet[ *i*  ] ここで  *、i*  = <1>、2、3、..  <br/> |
   
プログラムから、インデックスによって [Bullet] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  

