---
title: current 要素 (weatherType complexType) (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: 現在の気象条件を指定します。
ms.openlocfilehash: ce92bdd49ee37f939748586c2d63d8a664f664d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351472"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>current 要素 (weatherType complexType) (Outlook 天気情報スキーマ)

現在の気象条件を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[currenttype](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="current"      type="currentType">
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
|日付  <br/> |xs: date  <br/> |必須  <br/> |今日の日付を指定します。  <br/> |xs: date 型の値  <br/> |
|日勤  <br/> |xs: 文字列  <br/> |省略可能  <br/> |予測の日付を指定します。  <br/> |xs: 文字列型の値  <br/> |
|feelslike  <br/> |xs: 整数  <br/> |必須  <br/> |現在の天気予報の温度を指定します。  <br/> |xs: integer 型の値  <br/> |
|湿気  <br/> |xs: 整数  <br/> |必須  <br/> |現在の数値の湿度値を指定します。  <br/> |xs: integer 型の値  <br/> |
|observationpoint  <br/> |xs: 文字列  <br/> |必須  <br/> |現在の天気情報の参照先を指定します。  <br/> |xs: 文字列型の値  <br/> |
|observationtime  <br/> |xs: time  <br/> |必須  <br/> |現在の天気予報がどのような場合に観測されるかを指定します。  <br/> |xs: time 型の値  <br/> |
|短い日  <br/> |xs: 文字列  <br/> |省略可能  <br/> |日付を省略された形式で指定します。  <br/> |xs: 文字列型の値  <br/> |
|skycode  <br/> |xs: 整数  <br/> |必須  <br/> |現在の天気予報の整数コードを指定します。  <br/> |xs: integer 型の値  <br/> |
|skytext  <br/> |xs: 文字列  <br/> |必須  <br/> |現在の天気状況について、1 ~ 2 個の単語を指定します。  <br/> |xs: 文字列型の値  <br/> |
|変化  <br/> |xs: 整数  <br/> |必須  <br/> |場所の現在の温度を指定します。  <br/> |xs: integer 型の値  <br/> |
|winddisplay  <br/> |xs: 文字列  <br/> |必須  <br/> |現在の風向きに関する条件を表す文字列型 (string) の値を指定します。  <br/> |xs: 文字列型の値  <br/> |
|windspeed  <br/> |xs: 整数  <br/> |必須  <br/> |現在の数値の風向の速度の値を指定します。  <br/> |xs: integer 型の値  <br/> |
   

