---
title: Cell 要素 ([文字] セクション) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: フォント、色、スタイル、大文字/小文字、ベースラインに対する相対位置、またはポイントサイズなど、図形のテキストランの書式設定属性を指定します。
ms.openlocfilehash: 6dd895b33353944d27abb0d64a6a6df64ca19896
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356085"
---
# <a name="cell-element-character-section-visio-xml"></a>Cell 要素 ([文字] セクション) (' Visio XML ')

フォント、色、スタイル、大文字/小文字、ベースラインに対する相対位置、またはポイントサイズなど、図形のテキストランの書式設定属性を指定します。
  
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
|[Row 要素 (Character セクション)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |フォント、色、スタイル、大文字/小文字、ベースラインに対する相対位置、またはポイントサイズなど、図形のテキストランの書式設定属性を指定します。  <br/> |
   
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
|[asianfont]  <br/> |アジア言語の文字を含むテキストランの書式設定に使用するフォントの列挙が含まれています。  <br/> |[[AsianFont] セル ([Character] セクション)](asianfont-cell-character-section.md) <br/> |
|ケース  <br/> |図形のテキストランの大文字と小文字を指定します。  <br/> |[[Case] セル ([Character] セクション)](case-cell-character-section.md) <br/> |
|色  <br/> |図形のテキストの実行に使用する色を指定します。  <br/> |[[Color] セル ([Character] セクション)](color-cell-character-section.md) <br/> |
|colortrans  <br/> |レイヤーまたは図形のテキストランの色の透明度を指定します。 0 (完全に不透明) から 1 (完全に透明) です。  <br/> |なし。  <br/> |
|[complexscriptfont]  <br/> |コンプレックススクリプト文字で構成されるテキストランの書式設定に使用するフォントの番号が含まれています。  <br/> |[[ComplexScriptFont] セル ([Character] セクション)](complexscriptfont-cell-character-section.md) <br/> |
|[complexscriptsize]  <br/> |コンプレックススクリプト文字で構成されるテキストランの書式設定に使用するフォントのサイズです。  <br/> |[[ComplexScriptSize] セル ([Character] セクション)](complexscriptsize-cell-character-section.md) <br/> |
|dblunderline  <br/> |テキストランの範囲の下に二重下線を表示するかどうかを指定します。  <br/> |[[DoubleULine] セル ([Character] セクション)](doubleuline-cell-character-section.md) <br/> |
|[doublestrikethrough]  <br/> |テキストランが二重取り消し線として書式設定されるかどうかを指定します。  <br/> |[[DoubleStrikethrough] セル ([Character] セクション)](doublestrikethrough-cell-character-section.md) <br/> |
|フォント  <br/> |テキストランの書式設定に使用するフォントの番号を表します。  <br/> |[[Font] セル ([Character] セクション)](font-cell-character-section.md) <br/> |
|fontscale  <br/> |フォントの幅を指定します。  <br/> |なし。  <br/> |
|LangID  <br/> |テキストランが入力された言語を示します。  <br/> |[[LangID] セル ([Character] セクション)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |2つ以上の文字の間のスペースの量を指定します。 間隔は、1/20 ポイント単位で増減できます。  <br/> |なし。  <br/> |
|線  <br/> |テキストランの上に行を表示するかどうかを指定します。  <br/> |[[Overline] セル ([Character] セクション)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |ベースラインを基準にして、図形のテキストの実行位置を指定します。  <br/> |[[Pos] セル ([Character] セクション)](pos-cell-character-section.md) <br/> |
|サイズ  <br/> |図形のテキストブロックにあるテキストランのサイズを指定します。  <br/> |[[Size] セル ([Character] セクション)](size-cell-character-section.md) <br/> |
|[strikethru]  <br/> |テキストランが取り消し線として書式設定されるかどうかを指定します。  <br/> |[[Strikethru] セル ([Character] セクション)](strikethru-cell-character-section.md) <br/> |
|Style  <br/> |図形のテキストブロックにあるテキストランの範囲に適用される文字書式を表示します。  <br/> |[[Style] セル ([Character] セクション)](style-cell-character-section.md) <br/> |
   

