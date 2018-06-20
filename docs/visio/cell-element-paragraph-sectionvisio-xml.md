---
title: セル要素 (段落、セクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: 段落のインデント、行間隔、箇条書き、または段落の水平方向の配置などの図形のテキストの属性を指定します。
ms.openlocfilehash: 38309d3d1158b02084af6686c483547b28b8995f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804972"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>セル要素 (段落、セクション)'Visio XML (')

段落のインデント、行間隔、箇条書き、または段落の水平方向の配置などの図形のテキストの属性を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml、# .xml をマスター、# .xml のページ  <br/> |
   
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
|[行要素 ([Paragraph] セクション)](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |段落のインデント、行間隔、箇条書き、または段落の水平方向の配置などの図形のテキストの属性を指定します。  <br/> |
   
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
|行頭文字  <br/> |箇条書きのスタイルを指定します。  <br/> |[[Bullet] セル ([Paragraph] セクション)](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |ユーザー設定の箇条書き文字列を指定し、[Bullet] セルの値がゼロ以外のとき、テキストの書式設定に使用するフォントの番号を表します。  <br/> |[[BulletFont] セル ([Paragraph] セクション)](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |箇条書きのサイズを指定します。  <br/> |[[BulletSize] セル ([Paragraph] セクション)](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |箇条書きのスタイルをカスタマイズできます。  <br/> |[[BulletString] セル ([Paragraph] セクション)](bulletstring-cell-paragraph-section.md) <br/> |
|フラグ  <br/> |テキストの方向が左から右か、右から左かを示します。  <br/> |[[Flags] セル ([Paragraph] セクション)](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |図形のテキスト ブロックにあるテキストの水平方向の配置を指定します。  <br/> |[[HAlign] セル ([Paragraph] セクション)](halign-cell-paragraph-section.md) <br/> |
|[Indfirst]  <br/> |図形のテキスト ブロック内にある各段落の先頭行について、段落の左インデントからインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、先頭行のインデントは変わりません。  <br/> |[[IndFirst] セル ([Paragraph] セクション)](indfirst-cell-paragraph-section.md) <br/> |
|[Indleft]  <br/> |段落にあるテキストのすべての行について、テキスト ブロックの左余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、左インデントは変わりません。  <br/> |[[IndLeft] セル ([Paragraph] セクション)](indleft-cell-paragraph-section.md) <br/> |
|[Indright]  <br/> |段落にあるテキストのすべての行について、テキスト ブロックの右余白からインデントする距離を表します。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、右インデントは変わりません。  <br/> |[[IndRight] セル ([Paragraph] セクション)](indright-cell-paragraph-section.md) <br/> |
|[Spafter]  <br/> |図形のテキスト ブロック内にある各段落の後に挿入する間隔を指定します。この値に、[SpLine] セルや [BottomMargin] セル (テキスト ブロックの最後の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。  <br/> |[[SpAfter] セル ([Paragraph] セクション)](spafter-cell-paragraph-section.md) <br/> |
|[Spbefore]  <br/> |図形のテキスト ブロック内にある各段落の前に挿入する間隔を指定します。この値に、[SpLine] セルや [TopMargin] セル (テキスト ブロックの最初の段落に対して適用される) に指定した値が加えられて、テキスト ブロックが表示されます。  <br/> |[[SpBefore] セル ([Paragraph] セクション)](spbefore-cell-paragraph-section.md) <br/> |
|スプライン  <br/> |テキスト内の任意の行から次の行までの距離を、テキスト行の高さを 100% としてパーセントで表します。  <br/> |[[SpLine] セル ([Paragraph] セクション)](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |段落の第 1 行目と箇条書き行頭文字の間の距離を表します。  <br/> |[[TextPosAfterBullet] セル ([Paragraph] セクション)](textposafterbullet-cell-paragraph-section.md) <br/> |
   

