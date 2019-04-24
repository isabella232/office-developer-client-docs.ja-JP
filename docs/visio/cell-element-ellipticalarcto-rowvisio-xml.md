---
title: Cell 要素 ([ellipticalarcto] Row) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: 楕円の弧の端点の x 座標または y 座標、円弧のコントロールポイントの x 座標または y 座標、x 軸から楕円の長軸までの角度、または楕円の長軸と短軸との比率を格納します。
ms.openlocfilehash: 22dc813108d8f7b5b517c298c40c73ead8d4eec4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356071"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a>Cell 要素 ([ellipticalarcto] Row) (' Visio XML ')

楕円の弧の端点の x 座標または y 座標、円弧のコントロールポイントの x 座標または y 座標、x 軸から楕円の長軸までの角度、または楕円の長軸と短軸との比率を格納します。
  
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
|[Row 要素 (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[EllipticalArcTo_Type](ellipticalarcto_type-complextypevisio-xml.md) <br/> |楕円の弧の端点の x 座標または y 座標、円弧のコントロールポイントの x 座標または y 座標、x 軸から楕円の長軸までの角度、または楕円の長軸と短軸との比率を格納します。  <br/> |
   
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
|X  <br/> |円弧の最後の頂点に対する x 座標です。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |円弧の最後の頂点に対する y 座標です。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |円弧のコントロール ポイント (円弧上の点) に対する x 座標です。コントロール ポイントは円弧の開始の頂点と終了の頂点のほぼ中間に配置するのが最適な状態です。このような状態にない場合、コントロール ポイントを通過するために円弧が極端に大きくなり、予測できない結果が生じることがあります。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |円弧のコントロール ポイントの y 座標です。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |親図形の x 軸を基準にして、円弧の主軸の角度を示します。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
   

