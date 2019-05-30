---
title: weather 要素 (weatherdata 要素) (Outlook Weather Location スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: 気象を報告する場所を指定します。
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539013"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>weather 要素 (weatherdata 要素) (Outlook Weather Location スキーマ)

気象を報告する場所を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherlocation  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-location-schema.md) <br/> ||天気予報の要素を定義します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs: 文字列  <br/> |必須  <br/> |同じ名前の複数の場所を区別するために、場所に関連付けられているコードを指定します。  <br/> |Xs: 文字列型の値  <br/> |
|weatherlocationname  <br/> |xs: 文字列  <br/> |必須  <br/> |場所の名前を指定します。  <br/> |Xs: 文字列型の値  <br/> |
   

