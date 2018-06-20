---
title: セル要素 (EllipticalArcTo 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c0aa7a3-cc54-ffac-2c62-917b3d0a357e
description: X 座標または y 座標、楕円の円弧の終点の x 座標または y 座標のコントロールは、円弧、楕円の長軸、または比率を x 軸から楕円の長軸と短軸の軸間の角度のポイントが含まれます。
ms.openlocfilehash: 01d28fae5943251b61d0d26211ee91f09f25b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804966"
---
# <a name="cell-element-ellipticalarcto-row-visio-xml"></a>セル要素 (EllipticalArcTo 行) ('Visio XML')

X 座標または y 座標、楕円の円弧の終点の x 座標または y 座標のコントロールは、円弧、楕円の長軸、または比率を x 軸から楕円の長軸と短軸の軸間の角度のポイントが含まれます。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml をマスター、# .xml のページ  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[行要素 (ジオメトリ)](row-element-geometry-sectionvisio-xml.md) <br/> |[EllipticalArcTo_Type](ellipticalarcto_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、楕円の円弧の終点の x 座標または y 座標のコントロールは、円弧、楕円の長軸、または比率を x 軸から楕円の長軸と短軸の軸間の角度のポイントが含まれます。  <br/> |
   
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
|X  <br/> |円弧の終点の x 座標。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|Y  <br/> |円弧の終点の y 座標。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |円弧のコントロールの x 座標は、次のポイントです。円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で途中で最適に配置します。それ以外の場合、円弧は、予期しない結果で、コントロール ポイントを通過するために極端になることがあります。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |円弧のコントロール ポイントの y 座標。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |親図形の x 軸を基準にして、円弧の長軸の角度です。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |[[EllipticalArcTo] 行 ([Geometry] セクション)](ellipticalarcto-row-geometry-section.md) <br/> |
   

