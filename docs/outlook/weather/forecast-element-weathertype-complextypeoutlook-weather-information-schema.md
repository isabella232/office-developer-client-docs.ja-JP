---
title: forecast 要素 (weatherType complexType) (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540981"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>forecast 要素 (weatherType complexType) (Outlook 天気情報スキーマ)

今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[天気予報](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |場所の天気予報の条件を指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs: date  <br/> |必須  <br/> |予測の日付を指定します。  <br/> |Xs: date 型の値  <br/> |
|日勤  <br/> |xs: 文字列  <br/> |必須  <br/> |予測の日付を指定します。  <br/> |Xs: 文字列型の値  <br/> |
|高額  <br/> |xs: 整数  <br/> |必須  <br/> |予測最高温度を指定します。  <br/> |Xs: integer 型の値  <br/> |
|低さ  <br/> |xs: 整数  <br/> |必須  <br/> |予測される最低温度を指定します。  <br/> |Xs: integer 型の値  <br/> |
|precip  <br/> |xs: 整数  <br/> |必須  <br/> |降水のパーセンテージを指定します。  <br/> |Xs: integer 型の値  <br/> |
|短い日  <br/> |xs: 文字列  <br/> |必須  <br/> |日付を省略された形式で指定します。  <br/> |Xs: 文字列型の値  <br/> |
|skycodeday  <br/> |xs: 整数  <br/> |必須  <br/> |予測される条件のコードを指定します。  <br/> |Xs: integer 型の値  <br/> |
|skytextday  <br/> |xs: 文字列  <br/> |必須  <br/> |予測条件を説明する 1 ~ 2 単語を指定します。  <br/> |Xs: 文字列型の値  <br/> |
   

