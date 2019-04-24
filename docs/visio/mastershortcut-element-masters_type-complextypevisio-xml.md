---
title: mastershortcut 要素 (Masters_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: 図面で定義されているマスターシェイプのショートカットを指定します。
ms.openlocfilehash: 03196c6fc1f3424c61bcce406dc050f2d5a73365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341735"
---
# <a name="mastershortcut-element-masterstype-complextype-visio-xml"></a>mastershortcut 要素 (Masters_Type complexType) (' Visio XML ')

図面で定義されているマスターシェイプのショートカットを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|AlignName  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |ステンシルウィンドウ内の要素のテキストを左、右、または中央に配置するかどうかを指定します。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|IconSize  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |要素のアイコンのサイズ。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |親要素内の要素の一意の ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の名前。  <br/> |xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |xsd: string 型の値。  <br/> |
|PatternFlags  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |マスター シェイプをユーザー設定のパターンとして使用するかどうかを指定します。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|プロンプト  <br/> |xsd: string  <br/> |省略可能  <br/> |要素のステータスバーとツールヒントのプロンプト。  <br/> |xsd: string 型の値。  <br/> |
|ShortcutHelp  <br/> |xsd: string  <br/> |省略可能  <br/> |要素のヘルプ文字列。  <br/> |xsd: string 型の値。  <br/> |
|ShortcutURL  <br/> |xsd: string  <br/> |省略可能  <br/> |**mastershortcut**要素の URL。  <br/> |xsd: string 型の値。  <br/> |
   

