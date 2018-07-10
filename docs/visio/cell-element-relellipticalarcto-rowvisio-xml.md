---
title: セル要素 (RelEllipticalArcTo 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: X 座標または y 座標、図形の幅と高さを基準にして楕円の円弧の端点の基準にして図形の幅と高さ、角度、楕円の長軸、または間の比率を x 軸から円弧上の x 座標または y 座標のコントロール ポイントを含む、楕円の長軸と短軸の軸です。
ms.openlocfilehash: 661f6971ca4c03c68950ead45065bd12160918d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804985"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>セル要素 (RelEllipticalArcTo 行) ('Visio XML')

X 座標または y 座標、図形の幅と高さを基準にして楕円の円弧の端点の基準にして図形の幅と高さ、角度、楕円の長軸、または間の比率を x 軸から円弧上の x 座標または y 座標のコントロール ポイントを含む、楕円の長軸と短軸の軸です。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml をマスター、# .xml のページ  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[行要素 (ジオメトリ)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、図形の幅と高さを基準にして楕円の円弧の端点の基準にして図形の幅と高さ、角度、楕円の長軸、または間の比率を x 軸から円弧上の x 座標または y 座標のコントロール ポイントを含む、楕円の長軸と短軸の軸です。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|DurationFormat 要素  <br/> |xsd:string  <br/> |省略可能  <br/> |数式がエラーが発生することを示します。 **E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラー メッセージの文字列です。  <br/> |
|ExternalTaskProject 要素  <br/> |xsd:string  <br/> |省略可能  <br/> | 要素の式を表します。 この属性は、次の文字列のいずれかを含めることができます。  <br/>  '(いくつかの数式)' の数式がローカルに存在する場合  <br/>  `No Formula`数式がローカルで削除されるか、ブロックされている場合  <br/>  `Inh`場合は、数式が継承されます。  <br/> |数式です。  <br/> |
|MultipleCriticalPaths 要素  <br/> |xsd:string  <br/> |必須  <br/> |シェイプ シート セルの名前を表します。  <br/> |シェイプ シート セルの名前です。  <br/> 以下の「解説」セクションを参照してください。  <br/> |
|U  <br/> |xsd:string  <br/> |省略可能  <br/> |既定の測定単位を表しますが、DL です。  <br/> |セルの単位です。  <br/> |
|V  <br/> |xsd:string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |シェイプ シート セルの値です。  <br/> |
   
## <a name="remarks"></a>備考

この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。 この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細については**|
|:-----|:-----|:-----|
|X  <br/> |図形の幅を基準にして円弧の終点の x 座標。  <br/> |[RelEllipticalArcTo 行 ([Geometry] セクション)](relellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |図形の高さを基準にして円弧の終点の y 座標。  <br/> |[RelEllipticalArcTo 行 ([Geometry] セクション)](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |円弧のコントロールの x 座標は図形の幅を基準にしてポイントします。円弧上の点。  <br/> |[RelEllipticalArcTo 行 ([Geometry] セクション)](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |円弧のコントロールの y 座標は、図形の幅に対して相対的にポイントします。  <br/> |[RelEllipticalArcTo 行 ([Geometry] セクション)](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |親の x 軸を基準にして、円弧の長軸の角度です。  <br/> |[RelEllipticalArcTo 行 ([Geometry] セクション)](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |円弧の長軸と短軸の比率です。  <br/> |[RelEllipticalArcTo 行 ([Geometry] セクション)](relellipticalarcto-row-geometry-section.md) <br/> |
   
