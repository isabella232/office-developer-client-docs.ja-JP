---
title: Cell 要素 (Paragraph セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: 図形のテキストに対する、段落の書式属性を指定します。属性には、インデント、行間隔、箇条書き、または段落の水平方向の配置などがあります。
ms.openlocfilehash: adcbd3b595ffa579ecf2b1951ba7c96b9603a296
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594826"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Cell 要素 (Paragraph セクション) (Visio XML)

図形のテキストに対する、段落の書式属性を指定します。属性には、インデント、行間隔、箇条書き、または段落の水平方向の配置などがあります。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml、master#.xml、page#.xml  <br/> |
   
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
|[Row 要素 (Paragraph Section)](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |図形のテキストに対する、段落の書式属性を指定します。属性には、インデント、行間隔、箇条書き、または段落の水平方向の配置などがあります。  <br/> |
   
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
|行頭文字  <br/> |箇条書きのスタイルを指定します。  <br/> |[[Bullet] セル ([Paragraph] セクション)](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |ユーザー設定の箇条書き文字列を指定し、[Bullet] セルの値がゼロ以外のとき、テキストの書式設定に使用するフォントの番号を表します。  <br/> |[[BulletFont] セル ([Paragraph] セクション)](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |箇条書きのサイズを指定します。  <br/> |[[BulletSize] セル ([Paragraph] セクション)](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |箇条書きのスタイルをカスタマイズできます。  <br/> |[[BulletString] セル ([Paragraph] セクション)](bulletstring-cell-paragraph-section.md) <br/> |
|フラグ  <br/> |テキストの方向が左から右か、右から左かを示します。  <br/> |[[Flags] セル ([Paragraph] セクション)](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。  <br/> |[[HAlign] セル ([Paragraph] セクション)](halign-cell-paragraph-section.md) <br/> |
|IndFirst  <br/> |図形のテキスト ブロック内にある各段落の先頭行について、段落の左インデントからインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、先頭行のインデントは変わりません。  <br/> |[[IndFirst] セル ([Paragraph] セクション)](indfirst-cell-paragraph-section.md) <br/> |
|IndLeft  <br/> |段落にあるテキストのすべての行について、テキスト ブロックの左余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左インデントは変わりません。  <br/> |[[IndLeft] セル ([Paragraph] セクション)](indleft-cell-paragraph-section.md) <br/> |
|IndRight  <br/> |段落にあるテキストのすべての行について、テキスト ブロックの右余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右インデントは変わりません。  <br/> |[[IndRight] セル ([Paragraph] セクション)](indright-cell-paragraph-section.md) <br/> |
|SpAfter  <br/> |図形のテキスト ブロック内にある各段落の後に挿入する間隔を指定します。この値に、[SpLine] セルや [BottomMargin] セル (テキスト ブロックの最後の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。  <br/> |[[SpAfter] セル ([Paragraph] セクション)](spafter-cell-paragraph-section.md) <br/> |
|SpBefore  <br/> |図形のテキスト ブロック内にある各段落の前に挿入する間隔を指定します。この値に、[SpLine] セルや [TopMargin] セル (テキスト ブロックの最初の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。  <br/> |[[SpBefore] セル ([Paragraph] セクション)](spbefore-cell-paragraph-section.md) <br/> |
|SpLine  <br/> |テキスト内の任意の行から次の行までの距離を、テキスト行の高さを 100% としてパーセントで表します。  <br/> |[[SpLine] セル ([Paragraph] セクション)](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |段落の第 1 行目と箇条書き行頭文字の間の距離を表します。  <br/> |[[TextPosAfterBullet] セル ([Paragraph] セクション)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

