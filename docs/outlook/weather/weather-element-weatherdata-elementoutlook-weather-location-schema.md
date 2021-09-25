---
title: weather 要素 (weatherdata 要素) (Outlook天気予報の場所スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: 天気予報を報告する場所を指定します。
ms.openlocfilehash: 89b384579e1bfce38f75f573c642323db9d60cb5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570751"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>weather 要素 (weatherdata 要素) (Outlook天気予報の場所スキーマ)

天気予報を報告する場所を指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-location-schema.md) <br/> ||weather 要素を定義します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |必須出席者  <br/> |同じ名前の複数の場所を区別する場所に関連付けられているコードを指定します。  <br/> |xs:string 型の値  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |必須出席者  <br/> |場所の名前を指定します。  <br/> |xs:string 型の値  <br/> |
   

