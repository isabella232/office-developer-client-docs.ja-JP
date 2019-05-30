---
title: PageSheet 要素 (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: 図面ページに関連付けられた図面ページのプロパティを指定します。
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540624"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a>PageSheet 要素 (Page_Type complexType) (Visio XML)

図面ページに関連付けられた図面ページのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |ページの xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |文書内のページを定義する要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |塗りつぶしの書式設定を継承するスタイルシートの ID を指定します。 図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|LineStyle  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |線の書式設定を継承するスタイルシートの ID を指定します。 図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|TextStyle  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |テキストの書式設定を継承するスタイルシートの ID を指定します。 図面の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|UniqueID  <br/> |xsd: string  <br/> |省略可能  <br/> |親要素内の要素の一意の ID。  <br/> |Xsd: string 型の値。  <br/> |
   

