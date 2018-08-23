---
title: DocumentSheet 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: DocumentSheet 構造体を指定します。
ms.openlocfilehash: 50332759ff3bbe94887371d48c4a2e729243fb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805275"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSheet 要素 (VisioDocument_Type complexType)'Visio XML (')

DocumentSheet 構造体を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Microsoft Visio ドキュメントのルート要素です。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |DocumentSheet でセルを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |名前がユーザーによってカスタマイズされているかどうかについて説明します。  <br/> |Xsd:Boolean の値を入力します。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> |汎用名がユーザーによってカスタマイズされているかどうかについて説明します。  <br/> |Xsd:Boolean の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |DocumentSheet の言語に依存する名前を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |DocumentSheet の言語に依存しない名前を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |省略可能  <br/> |オプションの string。 図形を識別する GUID (グローバルに一意の識別子)。  <br/> |Xsd:string の値を入力します。  <br/> |
   

