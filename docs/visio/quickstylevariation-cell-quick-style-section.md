---
title: '[quickstylevariation] セル (クイックスタイルセクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: 図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはこれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを指定します。 0、1、2、4、および8のビット単位の値です。
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360015"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>[quickstylevariation] セル (クイックスタイルセクション)

図の背景と対照的な色を使用して、テキスト、線、塗りつぶしの色 (またはこれらのプロパティの組み合わせ) の数式と値を上書きするかどうかを指定します。 0、1、2、4、および8のビット単位の値です。
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |図形のテキスト、線、または塗りつぶしの色 (またはこれらのプロパティの組み合わせ) は変更しないでください。テーマの背景色に対して表示されたままになります。  <br/> |
|1-d  <br/> |図形のテキスト、線、または塗りつぶしの色 (またはこれらのプロパティの組み合わせ) は変更しないでください。テーマの背景色に対して表示されたままになります。  <br/> |
|pbm-2  <br/> |必要に応じて、図形のテキストの色を変更し、テーマの背景色に対して表示されたままにします。  <br/> |
|2/4  <br/> |必要に応じて、図形の線の色を変更し、テーマの背景色に対して表示されたままにします。  <br/> |
|~  <br/> |必要に応じて、図形の塗りつぶしの色を変更して、テーマの背景色に対して表示されたままにします。  <br/> |
   
## <a name="remarks"></a>解説

[quickstylevariation] セルを使用して、表示されている図形の図形の外側 (たとえば、ネットワーク図にある図形など) の外部にある場合に、テキストまたは行を表示します。 セルの既定値は0です。これは、その動作が非アクティブであることを意味します。 その他の値を指定すると、セルの動作がトリガーされます。
  
[quickstylevariation] の値は、色 (文字セクション)、[fillforegnd]、または linecolor] のいずれかのセルに配置されたときに、その関数によって生成された値よりも優先されます (または、これら3つのプロパティへの直接参照によって生成される)。文字の色 ")、評価 (" FillColor ")、および評価 (" linecolor] "))。
  
別の数式から、名前によって [ **[quickstylevariation]** ] セルへの参照を取得するには、 **cell**要素の**N**属性の値を取得するか、または**CellsU**プロパティを使用してプログラムから、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[quickstylevariation]  <br/> |
   
プログラムから、インデックスによって [ **[quickstylevariation]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
|セル インデックス:  <br/> |**visQuickStyleVariation** <br/> |
   

