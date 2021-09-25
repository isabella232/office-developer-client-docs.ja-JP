---
title: Cell 要素 (Controls Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: 図形に定義された特定のコントロール ハンドルのプロパティが含まれます。
ms.openlocfilehash: 45759522218736ddb6b08c3fd989658e08145fba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615985"
---
# <a name="cell-element-controls-row-visio-xml"></a>Cell 要素 (Controls Row) (Visio XML)

図形に定義された特定のコントロール ハンドルのプロパティが含まれます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Row 要素 ([コントロール] セクション)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |図形に定義された特定のコントロール ハンドルのプロパティが含まれます。  <br/> |
   
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
|CanGlue  <br/> |コントロール ハンドルを他の図形に接着できるかを指定します。  <br/> |[[Can Glue] セル ([Controls] セクション)](can-glue-cell-controls-section.md) <br/> |
|プロンプト  <br/> |ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを重ねたときに表示されます。  <br/> |[[Tip] セル ([Controls] セクション)](tip-cell-controls-section.md) <br/> |
|X  <br/> |図形のコントロール ハンドルの位置を示す x 座標を、ローカル座標で表します。  <br/> |[[X] セル ([Controls] セクション)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |ハンドルの移動後にコントロール ハンドルの x 座標が示す動作の種類を指定します。  <br/> |なし。  <br/> |
|xDyn  <br/> |コントロール ハンドルのアンカー ポイントの x 座標を、ローカル座標で表します。  <br/> |[[X Dynamics] セル ([Controls] セクション)](x-dynamics-cell-controls-section.md) <br/> |
|Y  <br/> |図形のコントロール ハンドルの位置を示す y 座標を、ローカル座標で表します。  <br/> |[[Y] セル ([Controls] セクション)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |ハンドルの移動後にコントロール ハンドルの y 座標が表示される動作の種類を指定します。  <br/> |なし。  <br/> |
|YDyn  <br/> |コントロール ハンドルのアンカー ポイントの y 座標を、ローカル座標で表します。  <br/> |[[Y Dynamics] セル ([Controls] セクション)](y-dynamics-cell-controls-section.md) <br/> |
   

