---
title: セル要素 (RelCubBezTo 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: daa5c527-65fe-a1e4-ab3e-24e77bdb522b
description: 図形の幅と高さの 3 次ベジエ曲線の端点、曲線の相対的な図形の幅と高さの最初の制御点の x 座標または y 座標の制御点の x 座標または y 座標の x 座標または y 座標が含まれています曲線の相対的な図形の幅と高さの終了します。
ms.openlocfilehash: e4a5353f3ecfb514b61ee893905e54c8951a2be5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804964"
---
# <a name="cell-element-relcubbezto-row-visio-xml"></a>セル要素 (RelCubBezTo 行) ('Visio XML')

図形の幅と高さの 3 次ベジエ曲線の端点、曲線の相対的な図形の幅と高さの最初の制御点の x 座標または y 座標の制御点の x 座標または y 座標の x 座標または y 座標が含まれています曲線の相対的な図形の幅と高さの終了します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
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
|[行要素 (ジオメトリ)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelCubBezTo_Type](relcubbezto_type-complextypevisio-xml.md) <br/> |図形の幅と高さの 3 次ベジエ曲線の端点、曲線の相対的な図形の幅と高さの最初の制御点の x 座標または y 座標の制御点の x 座標または y 座標の x 座標または y 座標が含まれています曲線の相対的な図形の幅と高さの終了します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |省略可能  <br/> |数式がエラーが発生することを示します。 **E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラー メッセージの文字列です。  <br/> |
|ExternalTaskProject 要素  <br/> |xsd:string  <br/> |省略可能  <br/> | 要素の式を表します。 この属性は、次の文字列のいずれかを含めることができます。  <br/>  '(いくつかの数式)' の数式がローカルに存在する場合  <br/>  `No Formula`数式がローカルで削除されるか、ブロックされている場合  <br/>  `Inh`場合は、数式が継承されます。  <br/> |数式です。  <br/> |
|N  <br/> |xsd:string  <br/> |必須  <br/> |シェイプ シート セルの名前を表します。  <br/> |シェイプ シート セルの名前です。  <br/> 以下の「解説」セクションを参照してください。  <br/> |
|U  <br/> |xsd:string  <br/> |省略可能  <br/> |既定の測定単位を表しますが、DL です。  <br/> |セルの単位です。  <br/> |
|V  <br/> |xsd:string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |シェイプ シート セルの値です。  <br/> |
   
## <a name="remarks"></a>注釈

この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。 この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|X  <br/> |図形の幅に相対する 3 次ベジエ曲線の最後の頂点の x 座標。  <br/> |[[RelCubBezTo] 行 ([図形座標] セクション)](relcubbezto-row-geometry-section.md) <br/> |
|Y  <br/> |図形の高さに相対する 3 次ベジエ曲線の最後の頂点の y 座標。  <br/> |[[RelCubBezTo] 行 ([図形座標] セクション)](relcubbezto-row-geometry-section.md) <br/> |
|A  <br/> |曲線の最初のコントロールの x 座標は図形の幅を基準にしてポイントします。円弧上の点。コントロール ポイントは、最初と最後の円弧の頂点の間で置くが最適です。  <br/> |[[RelCubBezTo] 行 ([図形座標] セクション)](relcubbezto-row-geometry-section.md) <br/> |
|B  <br/> |曲線の最初のコントロールの y 座標は、図形の高さに対して相対的なポイントです。  <br/> |[[RelCubBezTo] 行 ([図形座標] セクション)](relcubbezto-row-geometry-section.md) <br/> |
|C  <br/> |図形の幅を基準にして、曲線の終了の制御点の x 座標円弧上の点。コントロール ポイントは、円弧の先頭のコントロール ポイントおよび終了頂点の間で置くが最適です。  <br/> |[[RelCubBezTo] 行 ([図形座標] セクション)](relcubbezto-row-geometry-section.md) <br/> |
|D  <br/> |図形の高さを基準にして、曲線の終了の制御点の y 座標。  <br/> |[[RelCubBezTo] 行 ([図形座標] セクション)](relcubbezto-row-geometry-section.md) <br/> |
   

