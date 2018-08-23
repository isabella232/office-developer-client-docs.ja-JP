---
title: PublishSettings 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d0a41494-ffad-c56c-2074-135b3d0bffb9
description: Visio Services を使用して Microsoft SharePoint Server 2013 で、ダイアグラムを開いたときに使用する設定を指定します。
ms.openlocfilehash: f2554facc47de23104f65b26ae19cfc71821bd37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806131"
---
# <a name="publishsettings-element-visiodocumenttype-complextype-visio-xml"></a>PublishSettings 要素 (VisioDocument_Type complexType)'Visio XML (')

Visio Services を使用して Microsoft SharePoint Server 2013 で、ダイアグラムを開いたときに使用する設定を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[PublishSettings_Type](publishsettings_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="PublishSettings" type="PublishSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |図面のプロパティを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[PublishedPage](publishedpage-element-publishsettings_type-complextypevisio-xml.md) <br/> |[PublishedPage_Type](publishedpage_type-complextypevisio-xml.md) <br/> |図面ページは、Visio Services を使用してブラウザーで表示できるかどうかを指定します。  <br/> |
|[RefreshableData](refreshabledata-element-publishsettings_type-complextypevisio-xml.md) <br/> |[RefreshableData_Type](refreshabledata_type-complextypevisio-xml.md) <br/> |レコード セットは、Visio Services を使用してデータを更新するかどうかを指定します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

