---
title: '[SpLine] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
ms.localizationpriority: medium
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: テキスト内の任意の行から次の行までの距離を、テキスト行の高さを 100% としてパーセントで表します。
ms.openlocfilehash: 38a565eafcdd64da9fe4dfb041e76c584e392322
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553782"
---
# <a name="spline-cell-paragraph-section"></a>[SpLine] セル ([Paragraph] セクション)

テキスト内の任意の行から次の行までの距離を、テキスト行の高さを 100% としてパーセントで表します。
  
|**値**|**説明**|
|:-----|:-----|
| \>0  <br/> | フォント サイズに関係なく、絶対間隔になります。  <br/> |
| =0  <br/> | ベタ組みで設定されます (間隔 = フォント サイズの 100%)。  <br/> |
| \<0  <br/> | フォント サイズのパーセントです。たとえば -120% を指定すると、文字サイズの 120% で間隔が設定されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [SpLine] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Para。 SpLine [  *i*  ] ここで  *、i*  = <1>、2、3..  <br/> |
   
プログラムから、インデックスによって [SpLine] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visSpaceLine** <br/> |
   

