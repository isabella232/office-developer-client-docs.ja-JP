---
title: weather 要素 (weatherdata 要素) (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: 場所の天気予報の条件を指定します。
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541268"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>weather 要素 (weatherdata 要素) (Outlook 天気情報スキーマ)

場所の天気予報の条件を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-information-schema.md) <br/> ||天気予報の要素を定義します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[現在の](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |現在の気象条件を指定します。  <br/> |
|[気象](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|帰属  <br/> |xs: 文字列  <br/> |必須  <br/> |天気情報のソースを指定します。  <br/> |Xs: 文字列型の値  <br/> |
|degreetype  <br/> |xs: 文字列  <br/> |必須  <br/> |場所の温度の単位を指定します。たとえば、摂氏を指定します。  <br/> |C、F  <br/> |
|imagerelativeurl  <br/> |xs: 文字列  <br/> |必須  <br/> |場所のイメージの URL を指定します。  <br/> |Xs: 文字列型の値  <br/> |
|timezone  <br/> |xs: 整数  <br/> |必須  <br/> |GMT オフセットを指定します。  <br/> |-11 から12の範囲の値  <br/> |
|url  <br/> |xs: 文字列  <br/> |必須  <br/> |指定した場所の天気情報を含む天気予報サービスの web ページの URL を指定します。  <br/> |Xs: 文字列型の値  <br/> |
|weatherlocationcode  <br/> |xs: 文字列  <br/> |必須  <br/> |同じ名前を持つ複数の場所を区別するために使用される場所に関連付けられているコードを指定します。  <br/> |Xs: 文字列型の値  <br/> |
|weatherlocationname  <br/> |xs: 文字列  <br/> |必須  <br/> |ドロップダウンコントロールに表示される場所の名前を指定します。  <br/> |Xs: 文字列型の値  <br/> |
   

