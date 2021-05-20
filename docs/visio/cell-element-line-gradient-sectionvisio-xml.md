---
title: Cell 要素 ([線のグラデーション] セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8001249c-ea67-c5c0-3168-485400c43d8c
description: 線のグラデーションについて、グラデーションの分岐点の色、透過性、または位置を格納します。
ms.openlocfilehash: d8ac664285d24e47a142c22b1483e2ff435aef48
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539503"
---
# <a name="cell-element-line-gradient-section-visio-xml"></a>Cell 要素 ([線のグラデーション] セクション) (Visio XML)

線のグラデーションについて、グラデーションの分岐点の色、透過性、または位置を格納します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml、master#.xml、page#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Row 要素 ([線のグラデーション] セクション)](row-element-line-gradient-sectionvisio-xml.md) <br/> |[LineGradientRow_Type](linegradientrow_type-complextypevisio-xml.md) <br/> |線のグラデーションについて、グラデーションの分岐点の色、透過性、および位置を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |省略可能  <br/> |数式がエラーと評価されるかどうかを示します。 E の値 **は** 、現在の値 (エラー メッセージ文字列) です。V 属性の値 **は** 最後の有効な値です。  <br/> |エラー メッセージ文字列。  <br/> |
|F  <br/> |xsd:string  <br/> |省略可能  <br/> | 要素の数式を表します。 この属性には、次のいずれかの文字列を含めできます。  <br/>  式がローカルに存在する場合は'(一部の数式)'  <br/>  `No Formula` 数式がローカルで削除またはブロックされている場合  <br/>  `Inh` 数式が継承されている場合。  <br/> |数式。  <br/> |
|N  <br/> |xsd:string  <br/> |必須  <br/> |[シェイプシート] セルの名前を表します。  <br/> |[シェイプシート] セルの名前を指定します。  <br/> 以下の「備考」セクションを参照してください。  <br/> |
|U  <br/> |xsd:string  <br/> |省略可能  <br/> |測定単位を表します 既定は DL です。  <br/> |セルの単位。  <br/> |
|V  <br/> |xsd:string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |[シェイプシート] セルの値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

この **Cell** 要素の N 属性は **、ShapeSheet** セルに対応する制限された値のセットの 1 つである必要があります。 次の表を参照して、この Cell 要素で許可される **N** 属性の値を **決定** します。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|GradientStopColor  <br/> |グラデーションの分岐点の色の値。  <br/> |[[グラデーションの停止] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md) <br/> |
|GradientStopColorTrans  <br/> |グラデーションの停止色の透明度をパーセンテージで指定します。  <br/> |[[グラデーションの停止] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md) <br/> |
|GradientStopPosition  <br/> |グラデーションの位置は、グラデーションの原点からグラデーションの外側の端へのパーセンテージで、線のグラデーションの方向に沿って停止します。  <br/> |[[グラデーションの停止] 行 ([線のグラデーション] セクション)](gradient-stop-row-line-gradient-section.md) <br/> |
   

