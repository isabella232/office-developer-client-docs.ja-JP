---
title: MasterShortcut 要素 (Masters_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: ドキュメントで定義されているマスター シェイプのショートカットを指定します。
ms.openlocfilehash: be3e7d207e58d8c249598a7e156356d4f9e61849
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805835"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>MasterShortcut 要素 (Masters_Type complexType)'Visio XML (')

ドキュメントで定義されているマスター シェイプのショートカットを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |マスター # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |エンコードされたバイナリ] アイコン (.ico 形式) をドキュメント内の**マスター シェイプ**または**MasterShortcut**要素の MIME (多目的インターネット メール拡張機能) を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |ステンシル ウィンドウ内の要素のテキストが左、右揃えまたは中央揃えかどうかを指定します。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |要素のアイコンのサイズ。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |その親要素内の要素の一意の ID。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前です。  <br/> |Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名です。  <br/> |Xsd:string の値を入力します。  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |省略可能  <br/> |マスターのユーザー設定のパターンとして動作するかどうかを決定します。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|Prompt  <br/> |xsd:string  <br/> |省略可能  <br/> |ステータス バー、ツールは、要素の prompt ヒントです。  <br/> |Xsd:string の値を入力します。  <br/> |
|ShortcutHelp  <br/> |xsd:string  <br/> |省略可能  <br/> |要素のヘルプ文字列です。  <br/> |Xsd:string の値を入力します。  <br/> |
|ShortcutURL  <br/> |xsd:string  <br/> |省略可能  <br/> |**MasterShortcut**要素の URL です。  <br/> |Xsd:string の値を入力します。  <br/> |
   

