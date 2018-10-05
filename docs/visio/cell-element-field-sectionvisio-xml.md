---
title: セル要素 ([フィールド]) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: '[フィールド] ダイアログ ボックスを使用して図形のテキストに挿入した関数および数式を表示します。'
ms.openlocfilehash: f6c3c724b210ad579012ff58b93333e28c2a8cf1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383339"
---
# <a name="cell-element-field-section-visio-xml"></a>セル要素 ([フィールド]) ('Visio XML')

[フィールド] ダイアログ ボックスを使用して図形のテキストに挿入した関数および数式を表示します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Rowl 要素 ([フィールド] セクション)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |[フィールド] ダイアログ ボックスを使用して図形のテキストに挿入した関数および数式を表示します。  <br/> |
   
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
   
## <a name="remarks"></a>備考

この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。 この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|予定表  <br/> |データ型が Date のときに、テキスト フィールドに使用するカレンダーを指定します。  <br/> |[[Calendar] セル ([Text Fields] セクション)](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。  <br/> |[[Format] セル ([Text Fields] セクション)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |テキスト フィールドの種類を示します。  <br/> |[[ObjectKind] セル ([Text Fields] セクション)](objectkind-cell-text-fields-section.md) <br/> |
|種類  <br/> |テキスト フィールドの値に対してデータの種類を指定します。  <br/> |[[Type] セル ([Text Fields] セクション)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |挿入するフィールドのカテゴリを決定します。 フィールドとデータの書式設定ダイアログ ボックスでは、このセルを使用してフィールドとカテゴリの情報を決定します。  <br/> |[[UICategory] セル ([Text Fields] セクション)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |挿入するフィールドのコードを決定します。 フィールドとデータの書式設定ダイアログ ボックスでは、このセルを使用してフィールドとカテゴリの情報を決定します。  <br/> |[[UICode] セル ([Text Fields] セクション)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |挿入するフィールドの形式を決定します。 フィールドを決定するフィールドとデータの書式設定ダイアログ ボックスでこのセルを使用し、  <br/> |[[UIFormat] セル ([Text Fields] セクション)](uiformat-cell-text-fields-section.md) <br/> |
|値  <br/> |フィールドの関数が格納されます。  <br/> |[[Value] セル ([Text Fields] セクション)](value-cell-text-fields-section.md) <br/> |
   

