---
title: Cell 要素 ([relcubbezto] Row) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: daa5c527-65fe-a1e4-ab3e-24e77bdb522b
description: 図形の幅と高さに相対する3次ベジエ曲線の x 座標または y 座標、図形の幅と高さに相対する曲線の始点のコントロールポイントの x 座標または y 座標、またはコントロールポイントの x 座標または y 座標を格納します。図形の幅と高さを基準にして、曲線の終点の位置を示します。
ms.openlocfilehash: 15cfbbfd9b773169e338d7d364540582229a4ac7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339558"
---
# <a name="cell-element-relcubbezto-row-visio-xml"></a>Cell 要素 ([relcubbezto] Row) (' Visio XML ')

図形の幅と高さに相対する3次ベジエ曲線の x 座標または y 座標、図形の幅と高さに相対する曲線の始点のコントロールポイントの x 座標または y 座標、またはコントロールポイントの x 座標または y 座標を格納します。図形の幅と高さを基準にして、曲線の終点の位置を示します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |マスター # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Row 要素 (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelCubBezTo_Type](relcubbezto_type-complextypevisio-xml.md) <br/> |図形の幅と高さに相対する3次ベジエ曲線の x 座標または y 座標、図形の幅と高さに相対する曲線の始点のコントロールポイントの x 座標または y 座標、またはコントロールポイントの x 座標または y 座標を格納します。図形の幅と高さを基準にして、曲線の終点の位置を示します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: string  <br/> |省略可能  <br/> |数式がエラーとして評価されることを示します。 **E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラーメッセージ文字列。  <br/> |
|F  <br/> |xsd: string  <br/> |省略可能  <br/> | 要素の数式を表します。 この属性には、次のいずれかの文字列を含めることができます。  <br/>  ' (一部の数式) ' (数式がローカルに存在する場合)  <br/>  `No Formula`数式がローカルで削除またはブロックされている場合  <br/>  `Inh`数式が継承されている場合。  <br/> |数式。  <br/> |
|N  <br/> |xsd: string  <br/> |必須  <br/> |シェイプシートセルの名前を表します。  <br/> |シェイプシートセルの名前を指定します。  <br/> 下記の「備考」を参照してください。  <br/> |
|U  <br/> |xsd: string  <br/> |省略可能  <br/> |既定値は DL である計量単位を表します。  <br/> |セルの単位を示します。  <br/> |
|V  <br/> |xsd: string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |シェイプシートセルの値を指定します。  <br/> |
   
## <a name="remarks"></a>解説

この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。 この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|X  <br/> |図形の幅に相対する 3 次ベジエ曲線の最後の頂点の x 座標。  <br/> |[[relcubbezto] 行 (Geometry セクション)](relcubbezto-row-geometry-section.md) <br/> |
|Y  <br/> |図形の高さに相対する 3 次ベジエ曲線の最後の頂点の y 座標。  <br/> |[[relcubbezto] 行 (Geometry セクション)](relcubbezto-row-geometry-section.md) <br/> |
|A  <br/> |図形の幅を基準にした、曲線の開始位置を示す x 座標を指定します。弧の点を指定します。コントロールポイントは、円弧の始点と終点の間に配置するのが最適です。  <br/> |[[relcubbezto] 行 (Geometry セクション)](relcubbezto-row-geometry-section.md) <br/> |
|B  <br/> |図形の高さを基準にした、曲線の開始位置を示す y 座標です。  <br/> |[[relcubbezto] 行 (Geometry セクション)](relcubbezto-row-geometry-section.md) <br/> |
|C  <br/> |図形の幅を基準にした曲線の終了位置の x 座標を指定します。弧の点を指定します。コントロールポイントは、最初のコントロールポイントと円弧の最後の頂点の間に配置するのが最適です。  <br/> |[[relcubbezto] 行 (Geometry セクション)](relcubbezto-row-geometry-section.md) <br/> |
|D  <br/> |図形の高さを基準にした、曲線の終了位置の y 座標です。  <br/> |[[relcubbezto] 行 (Geometry セクション)](relcubbezto-row-geometry-section.md) <br/> |
   

