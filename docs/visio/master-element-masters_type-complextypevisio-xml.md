---
title: Master 要素 (Masters_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: 文書のマスターシェイプを定義する要素を格納します。
ms.openlocfilehash: f6effa521b7c5ea69d41b6770ee2dbef61af097c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283966"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Master 要素 (Masters_Type complexType) (' Visio XML ')

文書のマスターシェイプを定義する要素を格納します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |masters  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |文書の**マスター**要素を含みます。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |図面内の2つの図形を接続するための**Connect**要素を含みます。  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |ドキュメント内の**Master**または**mastershortcut**要素に対してエンコードされた、MIME (多目的インターネットメール内線) のエンコードされたバイナリアイコン (.ico 形式) を指定します。  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |**ページ**または**マスター**要素のページシートを定義する要素が含まれています。  <br/> |
|図形  <br/> |Shapes_Type  <br/> |**Shape**要素のコレクションを格納します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |ステンシルウィンドウ内のマスターシェイプのテキストを左、右、または中央に配置するかどうかを指定します。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|BaseID  <br/> |xsd: string  <br/> |省略可能  <br/> |ドキュメント間でマスターを識別する GUID (グローバル一意識別子)。  <br/> |xsd: string 型の値。  <br/> |
|Hidden  <br/> |xsd: boolean  <br/> |省略可能  <br/> |ユーザーインターフェイスでマスターシェイプを非表示にするかどうかを指定します。  <br/> |xsd: boolean 型の値。  <br/> |
|IconSize  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |要素のアイコンのサイズ。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|IconUpdate  <br/> |xsd: boolean  <br/> |省略可能  <br/> |マスターシェイプ自体からアイコンを自動生成するかどうかを指定します。  <br/> |xsd: boolean 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |親要素内の要素の一意の ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|MatchByName  <br/> |xsd: boolean  <br/> |省略可能  <br/> |図面ページにマスターシェイプのインスタンスがドロップされたときに図面マスターシェイプが既に存在するかどうかを決定する方法を指定します。  <br/> |xsd: boolean 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の名前。  <br/> |xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |xsd: string 型の値。  <br/> |
|PatternFlags  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |マスター シェイプをユーザー設定のパターンとして使用するかどうかを指定します。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|プロンプト  <br/> |xsd: string  <br/> |省略可能  <br/> |要素のステータスバーとツールヒントのプロンプト。  <br/> |xsd: string 型の値。  <br/> |
|UniqueID  <br/> |xsd: string  <br/> |省略可能  <br/> |ドキュメント内のマスターシェイプを識別する GUID。  <br/> |xsd: string 型の値。  <br/> |
   

