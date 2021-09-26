---
title: Master 要素 (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: ドキュメントのマスターを定義する要素が含まれます。
ms.openlocfilehash: 9bed3001bdf40fe54a32e6680c5de92a3035442f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603530"
---
# <a name="master-element-masters_type-complextype-visio-xml"></a>Master 要素 (Masters_Type complexType) (Visio XML)

ドキュメントのマスターを定義する要素が含まれます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |masters.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |ドキュメントの **Master** 要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |図面内の **2 Connect** 間の接続ごとに 1 つの要素を格納します。  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |ドキュメント内の Master 要素または **MasterShortcut** 要素の MIME (多目的インターネット メール拡張機能)エンコードされたバイナリ アイコン (.ico 形式) を指定します。  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Page または Master 要素のページ シートを定義 **する要素が****含** まれます。  <br/> |
|図形  <br/> |Shapes_Type  <br/> |Shape 要素のコレクション **を格納** します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |ステンシル ウィンドウのマスター テキストを左揃え、右揃え、中央揃えにするかどうかを指定します。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|BaseID  <br/> |xsd:string  <br/> |省略可能  <br/> |ドキュメント全体のマスターを識別する GUID (グローバルに一意の識別子)。  <br/> |xsd:string 型の値。  <br/> |
|Hidden  <br/> |xsd:boolean  <br/> |省略可能  <br/> |ユーザー インターフェイスでマスターマスターを非表示にするかどうかを指定します。  <br/> |xsd:boolean 型の値。  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |要素のアイコンのサイズ。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |省略可能  <br/> |アイコンがマスター自体から自動的に生成されるかどうかを指定します。  <br/> |xsd:boolean 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親要素内の要素の一意の ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |図面ページにマスター Visioがドロップされた場合に、ドキュメント マスターが既に存在するかどうかを Microsoft が判断する方法を決定します。  <br/> |xsd:boolean 型の値。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前。  <br/> |xsd:string 型の値。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |xsd:string 型の値。  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |マスター シェイプをユーザー設定のパターンとして使用するかどうかを指定します。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|プロンプト  <br/> |xsd:string  <br/> |省略可能  <br/> |要素のステータス バーとツール ヒントのプロンプト。  <br/> |xsd:string 型の値。  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |省略可能  <br/> |ドキュメント内のマスターを識別する GUID。  <br/> |xsd:string 型の値。  <br/> |
   

