---
title: 行要素 (ユーザー定義セル-部分) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: ユーザーが指定した 1 つの情報を他のセルやアドオン ツールによって参照できます。
ms.openlocfilehash: 10a0e0e5f7255274de528a34d5faa2de6137446e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806299"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a>行要素 (ユーザー定義セル-部分) ('Visio XML')

ユーザーが指定した 1 つの情報を他のセルやアドオン ツールによって参照できます。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[UserRow_Type](userrow_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml、masters.xml、マスターの # .xml、pages.xml ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[セクション](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |ユーザーが指定した 1 つの情報を他のセルやアドオン ツールによって参照できます。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |1 つのプロパティ、ユーザー指定の情報の他のセルやアドオン ツールによって参照できます。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |省略可能  <br/> |マスター シェイプから継承される行が削除されたかどうかを指定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |1 から始まる行の識別子を指定します。 特有である必要があり、同じセクションの他の識別子を超える。IX 属性は、文字、接続、フィールド、FillGradient、ジオメトリ、レイヤー、LineGradient、段落、校閲者、自由、およびタブのセクションでのみ使用します。 行は、IX または N の属性の 1 つだけ配置できます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|LocalName  <br/> |xsd:string  <br/> |省略可能  <br/> |行の一意の言語に依存する名前を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
|N  <br/> |xsd:string  <br/> |省略可能  <br/> |行の一意の言語に依存しない名前を指定します。N 属性は、ユーザー、プロパティ、動作、コントロール、接続、ハイパーリンク、および ActionTag のセクションでのみ使用します。 行は、IX または N の属性の 1 つだけ配置できます。  <br/> |Xsd:string の値を入力します。  <br/> |
|SV 要素  <br/> |xsd:string  <br/> |省略可能  <br/> |行によって表され、ジオメトリの視覚エフェクトで使用される幾何学的なパスの種類を指定します。 T 属性は、[Geometry] セクションでのみ使用します。  <br/> |Xsd:string の値を入力します。  <br/> |
   

