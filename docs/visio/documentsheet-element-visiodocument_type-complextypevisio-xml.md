---
title: DocumentSheet 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: DocumentSheet 構造を指定します。
ms.openlocfilehash: 279fca457163d5bcbdda885c11c589bfcde0baa9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540043"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSheet 要素 (VisioDocument_Type complexType) (Visio XML)

DocumentSheet 構造を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書の xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Microsoft Visio 図面のルート要素です。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |DocumentSheet のセルを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |xsd: boolean  <br/> |省略可能  <br/> |ユーザーによって名前がカスタマイズされているかどうかを示します。  <br/> |Xsd: Boolean 型の値。  <br/> |
|IsCustomNameU  <br/> |xsd: boolean  <br/> |省略可能  <br/> |ユーザーが汎用名をカスタマイズしたかどうかを示します。  <br/> |Xsd: Boolean 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |DocumentSheet の言語に依存する名前を指定します。  <br/> |Xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |省略可能  <br/> |DocumentSheet の言語に依存しない名前を指定します。  <br/> |Xsd: string 型の値。  <br/> |
|UniqueID  <br/> |xsd: string  <br/> |省略可能  <br/> |オプションの string。 図形を識別する GUID (グローバル一意識別子)。  <br/> |Xsd: string 型の値。  <br/> |
   

