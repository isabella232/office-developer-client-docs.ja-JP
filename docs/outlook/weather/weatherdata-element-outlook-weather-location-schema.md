---
title: weatherdata 要素 (Outlook の天気予報の場所のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: 気象要素を定義します。
ms.openlocfilehash: 5a3d0ed0fbf8d06472a6d9af727a41d97c0231cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804575"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a>weatherdata 要素 (Outlook の天気予報の場所のスキーマ)

気象要素を定義します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> ||
|**名前空間** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>定義

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[天気](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |天気をレポートする場所を指定します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

