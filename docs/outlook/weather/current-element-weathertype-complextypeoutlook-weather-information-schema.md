---
title: current 要素 (weatherType complexType) (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: 現在の気象条件を指定します。
ms.openlocfilehash: 1303212da1336112599ae5328498cca0d4ab5f89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541009"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>current 要素 (weatherType complexType) (Outlook天気予報スキーマ)

現在の気象条件を指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="current"      type="currentType">
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
|date  <br/> |xs:date  <br/> |必須  <br/> |今日の日付を指定します。  <br/> |xs:date 型の値  <br/> |
|日  <br/> |xs:string  <br/> |省略可能  <br/> |予測の日を指定します。  <br/> |xs:string 型の値  <br/> |
|感じが良い  <br/> |xs:integer  <br/> |必須  <br/> |現在の天気の温度を指定します。  <br/> |xs:integer 型の値  <br/> |
|湿度  <br/> |xs:integer  <br/> |必須  <br/> |現在の数値の湿度値を指定します。  <br/> |xs:integer 型の値  <br/> |
|オブザベーションポイント  <br/> |xs:string  <br/> |必須  <br/> |現在の気象情報の観測場所を指定します。  <br/> |xs:string 型の値  <br/> |
|観測時間  <br/> |xs:time  <br/> |必須  <br/> |現在の気象情報がいつ観測されるのか指定します。  <br/> |xs:time 型の値  <br/> |
|shortday  <br/> |xs:string  <br/> |省略可能  <br/> |省略形で日を指定します。  <br/> |xs:string 型の値  <br/> |
|skycode  <br/> |xs:integer  <br/> |必須  <br/> |現在の気象条件の整数コードを指定します。  <br/> |xs:integer 型の値  <br/> |
|skytext  <br/> |xs:string  <br/> |必須  <br/> |現在の気象条件を表す単語を 1 から 2 つ指定します。  <br/> |xs:string 型の値  <br/> |
|温度  <br/> |xs:integer  <br/> |必須  <br/> |場所の現在の温度を指定します。  <br/> |xs:integer 型の値  <br/> |
|winddisplay  <br/> |xs:string  <br/> |必須  <br/> |現在の風の状態を表す文字列。  <br/> |xs:string 型の値  <br/> |
|windspeed  <br/> |xs:integer  <br/> |必須  <br/> |現在の風速の数値を指定します。  <br/> |xs:integer 型の値  <br/> |
   

