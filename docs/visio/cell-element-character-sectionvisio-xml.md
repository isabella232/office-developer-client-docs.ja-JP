---
title: Cell 要素 (Character Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: フォント、色、スタイル、大文字と小文字、ベースラインに相対する位置、またはポイント サイズなどの図形のテキスト実行の書式属性を指定します。
ms.openlocfilehash: 1dea1b40afad75f59eb171b02dd102a9bcc97fb7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608544"
---
# <a name="cell-element-character-section-visio-xml"></a>Cell 要素 (Character Section) (Visio XML)

フォント、色、スタイル、大文字と小文字、ベースラインに相対する位置、またはポイント サイズなどの図形のテキスト実行の書式属性を指定します。
  
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
|[Row 要素 (Character Section)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |フォント、色、スタイル、大文字と小文字、ベースラインに相対する位置、またはポイント サイズなどの図形のテキスト実行の書式属性を指定します。  <br/> |
   
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
|AsianFont  <br/> |アジア文字を含むテキスト実行の書式設定に使用されるフォントの列挙を含む。  <br/> |[[AsianFont] セル ([Character] セクション)](asianfont-cell-character-section.md) <br/> |
|ケース  <br/> |図形のテキスト実行の大文字と小文字を指定します。  <br/> |[[Case] セル ([Character] セクション)](case-cell-character-section.md) <br/> |
|色  <br/> |図形のテキスト実行に使用する色を指定します。  <br/> |[[Color] セル ([Character] セクション)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |レイヤーまたは図形のテキストの実行色の透明度を 0 (完全に不透明) から 1 (完全に透明) に設定します。  <br/> |なし。  <br/> |
|ComplexScriptFont  <br/> |複雑なスクリプト文字で構成されるテキスト実行の書式設定に使用されるフォントの数を格納します。  <br/> |[[ComplexScriptFont] セル ([Character] セクション)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |複雑なスクリプト文字で構成されるテキスト実行の書式設定に使用されるフォントのサイズ。  <br/> |[[ComplexScriptSize] セル ([Character] セクション)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |テキストの実行範囲の下に二重の下線が付くかどうかを指定します。  <br/> |[[DoubleULine] セル ([Character] セクション)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |テキストの実行が二重取り消し線として書式設定されているかどうかを指定します。  <br/> |[[DoubleStrikethrough] セル ([Character] セクション)](doublestrikethrough-cell-character-section.md) <br/> |
|フォント  <br/> |テキストの実行の書式設定に使用するフォントの数を表します。  <br/> |[[Font] セル ([Character] セクション)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |フォント幅を指定します。  <br/> |なし。  <br/> |
|LangID  <br/> |テキストの実行が入力された言語を示します。  <br/> |[[LangID] セル ([Character] セクション)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |2 つ以上の文字の間のスペースの量を指定します。 間隔は、1/20 ポイント単位で増減できます。  <br/> |なし。  <br/> |
|オーバーライン  <br/> |テキスト実行の行の上に行を含めるかどうかを指定します。  <br/> |[[Overline] セル ([Character] セクション)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |基準線を基準に図形のテキストの実行位置を決定します。  <br/> |[[Pos] セル ([Character] セクション)](pos-cell-character-section.md) <br/> |
|Size  <br/> |図形のテキスト ブロックで実行されるテキストのサイズを指定します。  <br/> |[[Size] セル ([Character] セクション)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |テキストの実行が取り消し線として書式設定されているかどうかを指定します。  <br/> |[[Strikethru] セル ([Character] セクション)](strikethru-cell-character-section.md) <br/> |
|スタイル  <br/> |図形のテキスト ブロックで実行されるテキストの範囲に適用される文字の書式設定を表示します。  <br/> |[[Style] セル ([Character] セクション)](style-cell-character-section.md) <br/> |
   

