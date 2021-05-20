---
title: currentType complexType (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: 場所の現在の気象条件に関するパラメーターを定義します。
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540988"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (Outlook天気予報スキーマ)

場所の現在の気象条件に関するパラメーターを定義します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
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
   

