---
title: forecast 要素 (weatherType complexType) (Outlook 天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 今日、明日、明日の次の日を含む、少なくとも 3 日先の将来の気象条件を指定します。
ms.openlocfilehash: 51a4df8c1ee711cb10db70d631ef93edb7d1c356
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549638"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>forecast 要素 (weatherType complexType) (Outlook 天気予報スキーマ)

今日、明日、明日の次の日を含む、少なくとも 3 日先の将来の気象条件を指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[天気](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |場所の気象条件を指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |必須出席者  <br/> |予測の日付を指定します。  <br/> |xs:date 型の値  <br/> |
|日  <br/> |xs:string  <br/> |必須  <br/> |予測の日を指定します。  <br/> |xs:string 型の値  <br/> |
|high  <br/> |xs:integer  <br/> |必須  <br/> |予測される最高温度を指定します。  <br/> |xs:integer 型の値  <br/> |
|low  <br/> |xs:integer  <br/> |必須  <br/> |予測される最低温度を指定します。  <br/> |xs:integer 型の値  <br/> |
|precip  <br/> |xs:integer  <br/> |必須  <br/> |降水の可能性の割合を指定します。  <br/> |xs:integer 型の値  <br/> |
|shortday  <br/> |xs:string  <br/> |必須  <br/> |省略形で日を指定します。  <br/> |xs:string 型の値  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |必須  <br/> |予測条件のコードを指定します。  <br/> |xs:integer 型の値  <br/> |
|skytextday  <br/> |xs:string  <br/> |必須  <br/> |予測条件を表す 1 から 2 つの単語を指定します。  <br/> |xs:string 型の値  <br/> |
   

