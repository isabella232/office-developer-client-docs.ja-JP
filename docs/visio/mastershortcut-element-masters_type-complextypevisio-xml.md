---
title: MasterShortcut 要素 (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: 図面で定義されているマスターシェイプのショートカットを指定します。
ms.openlocfilehash: 94ac64ff0080bf7d50df67674022ce53f32339a4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538208"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>MasterShortcut 要素 (Masters_Type complexType) (Visio XML)

図面で定義されているマスターシェイプのショートカットを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |マスター # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
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
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |ドキュメント内の**Master**または**mastershortcut**要素に対してエンコードされた、MIME (多目的インターネットメール内線) のエンコードされたバイナリアイコン (.ico 形式) を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> |ステンシルウィンドウ内の要素のテキストを左、右、または中央に配置するかどうかを指定します。  <br/> |Xsd: _ Signedshort 型の値。  <br/> |
|IconSize  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> |要素のアイコンのサイズ。  <br/> |Xsd: _ Signedshort 型の値。  <br/> |
|ID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |親要素内の要素の一意の ID。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の名前。  <br/> |Xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |Xsd: string 型の値。  <br/> |
|PatternFlags  <br/> |xsd: アン Signedshort  <br/> |省略可能  <br/> |マスター シェイプをユーザー設定のパターンとして使用するかどうかを指定します。  <br/> |Xsd: _ Signedshort 型の値。  <br/> |
|プロンプト  <br/> |xsd: string  <br/> |省略可能  <br/> |要素のステータスバーとツールヒントのプロンプト。  <br/> |Xsd: string 型の値。  <br/> |
|ShortcutHelp  <br/> |xsd: string  <br/> |省略可能  <br/> |要素のヘルプ文字列。  <br/> |Xsd: string 型の値。  <br/> |
|ShortcutURL  <br/> |xsd: string  <br/> |省略可能  <br/> |**Mastershortcut**要素の URL。  <br/> |Xsd: string 型の値。  <br/> |
   

