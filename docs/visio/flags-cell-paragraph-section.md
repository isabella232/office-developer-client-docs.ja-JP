---
title: '[Flags] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: テキストの方向が左から右か、右から左かを示します。
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413116"
---
# <a name="flags-cell-paragraph-section"></a>[Flags] セル ([Paragraph] セクション)

テキストの方向が左から右か、右から左かを示します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |テキストの方向は、左から右です (既定値)。  <br/> |
|1  <br/> |テキストの方向は、右から左です。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[テキスト]ダイアログ ボックスの [段落]タブの [方向] 設定に対応します ([ホーム] タブの [フォント] 矢印をクリックします)。これは、**複雑** なスクリプト テキストを使用する言語が Microsoft Office の [言語の基本設定] ダイアログ ボックスに追加されている場合にのみ表示されます。   ([**スタート] ボタン**、[すべてのプログラム **]** の順にクリックし、[Microsoft Office]**をクリック** し、[Microsoft Office **ツール**] をクリックし、[言語の基本設定] をMicrosoft Office **クリック** します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Flags] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Para.Flags[ *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Flags] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
|行インデックス:  <br/> |**visRowParagraph**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visFlags** <br/> |
   

