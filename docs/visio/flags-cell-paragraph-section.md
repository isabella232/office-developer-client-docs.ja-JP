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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346222"
---
# <a name="flags-cell-paragraph-section"></a>[Flags] セル ([Paragraph] セクション)

テキストの方向が左から右か、右から左かを示します。
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |テキストの方向は、左から右です (既定値)。  <br/> |
|1-d  <br/> |テキストの方向は、右から左です。  <br/> |
   
## <a name="remarks"></a>解説

このセルの値は、[**テキスト**] ダイアログボックスの [段落] タブ ([**ホーム**] タブの [**フォント**] 矢印をクリックすると表示されます) の [**段落**] タブでの**方向**の設定に対応しています。これは、コンプレックススクリプトのテキストを使用する言語が次の場合にのみ表示されます。[ **Microsoft Office 言語設定**] ダイアログボックスに追加されました。 ([**スタート**]、 **[すべてのプログラム**]、[ **microsoft office**]、[microsoft office**ツール**]、[ **microsoft office の言語設定**] の順にクリックします)。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Flags] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |<1> [ *i* ]、 *i* =、2、3...  <br/> |
   
プログラムから、インデックスによって [Flags] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
|行インデックス:  <br/> |**visRowParagraph** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visFlags** <br/> |
   

