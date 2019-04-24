---
title: Cell 要素 ([段落] セクション) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: インデント、行間、箇条書き、段落の水平方向の配置など、図形のテキストの段落書式属性を指定します。
ms.openlocfilehash: 2647ce92b38234e4d6fc4d6bc59188d468332ca8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344843"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Cell 要素 ([段落] セクション) (' Visio XML ')

インデント、行間、箇条書き、段落の水平方向の配置など、図形のテキストの段落書式属性を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書 .xml、master # .xml、ページ # .xml  <br/> |
   
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
|[Row 要素 (Paragraph セクション)](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |インデント、行間、箇条書き、段落の水平方向の配置など、図形のテキストの段落書式属性を指定します。  <br/> |
   
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
|行頭文字  <br/> |箇条書きのスタイルを指定します。  <br/> |[[Bullet] セル ([Paragraph] セクション)](bullet-cell-paragraph-section.md) <br/> |
|[bulletfont]  <br/> |ユーザー設定の箇条書き文字列を指定し、[Bullet] セルの値がゼロ以外のとき、テキストの書式設定に使用するフォントの番号を表します。  <br/> |[[BulletFont] セル ([Paragraph] セクション)](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |箇条書きのサイズを指定します。  <br/> |[[BulletSize] セル ([Paragraph] セクション)](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |箇条書きのスタイルをカスタマイズできます。  <br/> |[[BulletString] セル ([Paragraph] セクション)](bulletstring-cell-paragraph-section.md) <br/> |
|フラグ  <br/> |テキストの方向が左から右か、右から左かを示します。  <br/> |[[Flags] セル ([Paragraph] セクション)](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。  <br/> |[[HAlign] セル ([Paragraph] セクション)](halign-cell-paragraph-section.md) <br/> |
|[indfirst]  <br/> |図形のテキスト ブロック内にある各段落の先頭行について、段落の左インデントからインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、先頭行のインデントは変わりません。  <br/> |[[IndFirst] セル ([Paragraph] セクション)](indfirst-cell-paragraph-section.md) <br/> |
|[indleft]  <br/> |段落にあるテキストのすべての行について、テキスト ブロックの左余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左インデントは変わりません。  <br/> |[[IndLeft] セル ([Paragraph] セクション)](indleft-cell-paragraph-section.md) <br/> |
|[indright]  <br/> |段落にあるテキストのすべての行について、テキスト ブロックの右余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右インデントは変わりません。  <br/> |[[IndRight] セル ([Paragraph] セクション)](indright-cell-paragraph-section.md) <br/> |
|[spafter]  <br/> |図形のテキスト ブロック内にある各段落の後に挿入する間隔を指定します。この値に、[SpLine] セルや [BottomMargin] セル (テキスト ブロックの最後の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。  <br/> |[[SpAfter] セル ([Paragraph] セクション)](spafter-cell-paragraph-section.md) <br/> |
|[spbefore]  <br/> |図形のテキスト ブロック内にある各段落の前に挿入する間隔を指定します。この値に、[SpLine] セルや [TopMargin] セル (テキスト ブロックの最初の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。  <br/> |[[SpBefore] セル ([Paragraph] セクション)](spbefore-cell-paragraph-section.md) <br/> |
|スプライン  <br/> |テキスト内の任意の行から次の行までの距離を、テキスト行の高さを 100% としてパーセントで表します。  <br/> |[[SpLine] セル ([Paragraph] セクション)](spline-cell-paragraph-section.md) <br/> |
|[textposafterbullet]  <br/> |段落の第 1 行目と箇条書き行頭文字の間の距離を表します。  <br/> |[[TextPosAfterBullet] セル ([Paragraph] セクション)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

