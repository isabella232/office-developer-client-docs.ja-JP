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
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805387"
---
# <a name="flags-cell-paragraph-section"></a>[Flags] セル ([段落] セクション)

テキストの方向が左から右か、右から左かを示します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |テキストの方向は、左から右です (既定値)。  <br/> |
|1  <br/> |テキストの方向は、右から左です。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**段落**] タブ、[**テキスト**] ダイアログ ボックスで、**方向**の設定に対応して ([**ホーム**] タブで、矢印をクリック、**フォント**) されている場合は、複雑なを使用する言語のスクリプトのテキストを表示します。**Microsoft Office 言語設定**] ダイアログ ボックスに追加されます。 ([**スタート**] ボタン [**すべてのプログラム**] をクリックして、 **Microsoft Office**、 **Microsoft Office ツール**] をクリックして、 **Microsoft Office 言語設定**] をクリックします。) 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Flags] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Para.Flags [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Flags] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
|行インデックス:  <br/> |**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visFlags** <br/> |
   

