---
title: '[Bullet] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: 箇条書きのスタイルを指定します。
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338193"
---
# <a name="bullet-cell-paragraph-section"></a>[Bullet] セル ([Paragraph] セクション)

箇条書きのスタイルを指定します。
  
|**値**|**箇条書きのスタイル**|
|:-----|:-----|
|.0  <br/> |None  <br/> |
|1-d  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|pbm-2  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|1/3  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|2/4  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|5  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|シックス  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|7  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
|行インデックス:  <br/> |**visRowParagraph** +  *i* = ** 0、1、2、...  <br/> |
|セル インデックス:  <br/> |**visBulletIndex** <br/> |
   
## <a name="remarks"></a>解説

このセルの値は、図形を右クリックして [**書式**] をポイントし、[**テキスト**]、[**箇条書き**] の順にクリックして設定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Bullet] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |段落記号 [ *i* ] = <1> ** 、2、3、...  <br/> |
   
プログラムから、インデックスによって [Bullet] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  

