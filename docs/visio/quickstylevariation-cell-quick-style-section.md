---
title: '[QuickStyleVariation] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: 図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはそれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを決定します。 値は、0、1、2、4、および 8 のビット形式の OR です。
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433795"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>[QuickStyleVariation] セル ([クイック スタイル] セクション)

図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはそれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを決定します。 値は、0、1、2、4、および 8 のビット形式の OR です。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |図形のテキスト、線、塗りつぶしの色 (またはそれらのプロパティの任意の組み合わせ) を変更して、テーマの特定の背景色に対して表示されたままにしない。  <br/> |
|1  <br/> |図形のテキスト、線、塗りつぶしの色 (またはそれらのプロパティの任意の組み合わせ) を変更して、テーマの特定の背景色に対して表示されたままにしない。  <br/> |
|2  <br/> |必要に応じて、図形のテキストの色を変更して、テーマの指定された背景色に対して表示されたままにします。  <br/> |
|4  <br/> |必要に応じて図形の線の色を変更して、テーマの指定された背景色に対して表示されたままにします。  <br/> |
|8  <br/> |必要に応じて、図形の塗りつぶしの色を変更して、テーマの指定された背景色に対して表示されたままにします。  <br/> |
   
## <a name="remarks"></a>注釈

[QuickStyleVariation] セルを使用して、表示されている図形ジオメトリの外側にあるテキストまたは線の表示を保証します (たとえば、テキスト ボックスが図形の下部 (ネットワーク ダイアグラムなど) の下にある図形の場合)。 セルの既定値は 0 で、その動作は非アクティブです。 その他の値を指定すると、セルの動作がトリガーされます。
  
QuickStyleVariation 値は、THEMEVAL 関数が Color (Character Section)、FillForegnd、または LineColor セルに存在する場合 (または THEMEVAL("CharacterColor")、THEMEVAL("FillColor"))、THEMEVAL("LineColor") を使用してこれら 3 つのプロパティへの直接参照によって生成される場合に、THEMEVAL 関数によって生成される値を上書きします。
  
別の数式から名前によって **[QuickStyleVariation]** セルへの参照を取得するには、Cell 要素の **N** 属性の値を取得するか **、CellsU** プロパティを使用してプログラムから取得します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |QuickStyleVariation  <br/> |
   
プログラムからインデックスによって **[QuickStyleVariation]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
|セル インデックス:  <br/> |**visQuickStyleVariation** <br/> |
   

