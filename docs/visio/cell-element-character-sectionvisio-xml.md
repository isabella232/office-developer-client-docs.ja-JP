---
title: セル要素 ([Character] セクション) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: フォント、色、スタイル、ケース、ベースラインに相対位置またはポイント サイズなど、図形のテキスト ランの書式設定属性を指定します。
ms.openlocfilehash: 0d0725ec6ff19104d95780dcfbb3fff9715cbe92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804952"
---
# <a name="cell-element-character-section-visio-xml"></a>セル要素 ([Character] セクション) ('Visio XML')

フォント、色、スタイル、ケース、ベースラインに相対位置またはポイント サイズなど、図形のテキスト ランの書式設定属性を指定します。
  
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
|[行要素 ([Character] セクション)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |フォント、色、スタイル、ケース、ベースラインに相対位置またはポイント サイズなど、図形のテキスト ランの書式設定属性を指定します。  <br/> |
   
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
|[Asianfont]  <br/> |アジア言語の文字が含まれているを実行するテキストを書式設定に使用するフォントの列挙体が含まれています。  <br/> |[[AsianFont] セル ([Character] セクション)](asianfont-cell-character-section.md) <br/> |
|ケース  <br/> |実行する図形のテキストの大文字と小文字を決定します。  <br/> |[[Case] セル ([Character] セクション)](case-cell-character-section.md) <br/> |
|色  <br/> |図形のテキストの実行に使用する色を決定します。  <br/> |[[Color] セル ([Character] セクション)](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |レイヤーまたは図形のテキストの色は 0 (完全に不透明) から 1 (完全に透明) からの透明度を決定します。  <br/> |なし。  <br/> |
|ComplexScriptFont  <br/> |複雑なスクリプトの文字から成るテキストを書式設定に使用するフォントの数が含まれています。  <br/> |[[ComplexScriptFont] セル ([Character] セクション)](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |複雑なスクリプトの文字から成るテキストを書式設定に使用するフォントのサイズを実行します。  <br/> |[[ComplexScriptSize] セル ([Character] セクション)](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |テキスト ランの範囲に二重下線が含まれているかどうかを決定します。  <br/> |[[DoubleULine] セル ([Character] セクション)](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |テキスト ランが二重取り消し線として書式設定されたかどうかを決定します。  <br/> |[[DoubleStrikethrough] セル ([Character] セクション)](doublestrikethrough-cell-character-section.md) <br/> |
|フォント  <br/> |テキスト ランの書式設定に使用するフォントの数を表します。  <br/> |[[Font] セル ([Character] セクション)](font-cell-character-section.md) <br/> |
|FontScale  <br/> |フォントの幅を指定します。  <br/> |なし。  <br/> |
|LangID  <br/> |テキスト ランの入力に使用された言語を示します。  <br/> |[[LangID] セル ([Character] セクション)](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |2 つ以上の文字間のスペースの量を指定します。 領域を追加または 1/20 ポイント単位で差し引かれることができます。  <br/> |なし。  <br/> |
|上線  <br/> |テキスト ランに上線があるかどうかを決定します。  <br/> |[[Overline] セル ([Character] セクション)](overline-cell-character-section.md) <br/> |
|Pos  <br/> |ベースラインを基準として実行する図形のテキストの位置を決定します。  <br/> |[[Pos] セル ([Character] セクション)](pos-cell-character-section.md) <br/> |
|サイズ  <br/> |図形のテキスト ブロックのテキストのサイズを決定します。  <br/> |[[Size] セル ([Character] セクション)](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |テキスト ランが取り消し線として書式設定されたかどうかを決定します。  <br/> |[[Strikethru] セル ([Character] セクション)](strikethru-cell-character-section.md) <br/> |
|スタイル  <br/> |図形のテキスト ブロック内のテキスト範囲に適用される文字書式の表示を実行します。  <br/> |[[Style] セル ([Character] セクション)](style-cell-character-section.md) <br/> |
   

