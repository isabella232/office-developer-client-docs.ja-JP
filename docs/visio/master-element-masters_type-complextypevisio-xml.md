---
title: マスター要素 (Masters_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: ドキュメントのマスターを定義する要素が含まれています。
ms.openlocfilehash: 51c5f0ad8bee5000e981fcfd4d15e2e49f2bda3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805829"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>マスター要素 (Masters_Type complexType)'Visio XML (')

ドキュメントのマスターを定義する要素が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |masters.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[マスター](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |ドキュメントの**マスター**の要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[接続](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |図面内の 2 つの図形間の各接続の**接続**の要素が含まれています。  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |エンコードされたバイナリ] アイコン (.ico 形式) をドキュメント内の**マスター シェイプ**または**MasterShortcut**要素の MIME (多目的インターネット メール拡張機能) を指定します。  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |**マスター シェイプ**または**ページ**の要素のページ シートを定義する要素が含まれています。  <br/> |
|Shapes  <br/> |Shapes_Type  <br/> |**図形**要素のコレクションが含まれています。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |ステンシル ウィンドウでマスター シェイプのテキストが左、右揃えまたは中央揃えかどうかを指定します。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|BaseID  <br/> |xsd:string  <br/> |省略可能  <br/> |ドキュメントのマスターを識別する GUID (グローバル一意識別子) です。  <br/> |Xsd:string の値を入力します。  <br/> |
|非表示  <br/> |xsd:boolean  <br/> |省略可能  <br/> |ユーザー インターフェイスで、マスターが非表示かどうかを指定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |要素のアイコンのサイズ。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |省略可能  <br/> |マスター シェイプ自体から、アイコンを自動的に生成するかどうかを指定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |その親要素内の要素の一意の ID。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |マスターが図面ページにドロップされた図面マスター シェイプが既に場合のインスタンスに存在する場合を Microsoft Visio が決定する方法を決定します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前です。  <br/> |Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名です。  <br/> |Xsd:string の値を入力します。  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |マスターのユーザー設定のパターンとして動作するかどうかを決定します。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|Prompt  <br/> |xsd:string  <br/> |省略可能  <br/> |ステータス バー、ツールは、要素の prompt ヒントです。  <br/> |Xsd:string の値を入力します。  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |省略可能  <br/> |ドキュメント内のマスターを識別する GUID です。  <br/> |Xsd:string の値を入力します。  <br/> |
   

