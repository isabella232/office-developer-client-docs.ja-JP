---
title: 行要素 ([Character] セクション) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 764a8e77-5308-e6ce-8763-dc6e6090da9d
description: 、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。
ms.openlocfilehash: 11194506a593a445656852b107f6fd780a39b9b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806265"
---
# <a name="row-element-character-section-visio-xml"></a>行要素 ([Character] セクション) ('Visio XML')

、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml、# .xml をマスター、# .xml のページ  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Row" type="CharacterRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |、ベースラインからの相対位置し、ポイント サイズを示していますが、フォント、色、テキストのスタイル、大文字と小文字など、図形のテキストの書式設定属性を実行します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |省略可能  <br/> |マスター シェイプから継承される行が削除されたかどうかを指定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |1 から始まる行の識別子を指定します。 特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。 行は、IX または N の属性の 1 つだけ配置できます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|LocalName  <br/> |xsd:string  <br/> |省略可能  <br/> |行の一意の言語に依存する名前を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
|MultipleCriticalPaths 要素  <br/> |xsd:string  <br/> |省略可能  <br/> |行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。 行は、IX または N の属性の 1 つだけ配置できます。  <br/> |Xsd:string の値を入力します。  <br/> |
|SV 要素  <br/> |xsd:string  <br/> |省略可能  <br/> |行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。 T 属性は、[Geometry] セクションでのみ使用します。  <br/> |Xsd:string の値を入力します。  <br/> |
   
