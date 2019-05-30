---
title: currentType complexType (Outlook Weather Information スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: 場所の現在の天気状況に関するパラメーターを定義します。
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540988"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (Outlook Weather Information スキーマ)

場所の現在の天気状況に関するパラメーターを定義します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo  <br/> |
|**拡張ベース** <br/> |None  <br/> |
   
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

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs: date  <br/> |必須  <br/> |今日の日付を指定します。  <br/> |Xs: date 型の値  <br/> |
|日勤  <br/> |xs: 文字列  <br/> |省略可能  <br/> |予測の日付を指定します。  <br/> |Xs: 文字列型の値  <br/> |
|feelslike  <br/> |xs: 整数  <br/> |必須  <br/> |現在の天気予報の温度を指定します。  <br/> |Xs: integer 型の値  <br/> |
|湿気  <br/> |xs: 整数  <br/> |必須  <br/> |現在の数値の湿度値を指定します。  <br/> |Xs: integer 型の値  <br/> |
|observationpoint  <br/> |xs: 文字列  <br/> |必須  <br/> |現在の天気情報の参照先を指定します。  <br/> |Xs: 文字列型の値  <br/> |
|observationtime  <br/> |xs: time  <br/> |必須  <br/> |現在の天気予報がどのような場合に観測されるかを指定します。  <br/> |Xs: time 型の値  <br/> |
|短い日  <br/> |xs: 文字列  <br/> |省略可能  <br/> |日付を省略された形式で指定します。  <br/> |Xs: 文字列型の値  <br/> |
|skycode  <br/> |xs: 整数  <br/> |必須  <br/> |現在の天気予報の整数コードを指定します。  <br/> |Xs: integer 型の値  <br/> |
|skytext  <br/> |xs: 文字列  <br/> |必須  <br/> |現在の天気状況について、1 ~ 2 個の単語を指定します。  <br/> |Xs: 文字列型の値  <br/> |
|変化  <br/> |xs: 整数  <br/> |必須  <br/> |場所の現在の温度を指定します。  <br/> |Xs: integer 型の値  <br/> |
|winddisplay  <br/> |xs: 文字列  <br/> |必須  <br/> |現在の風向きに関する条件を表す文字列型 (string) の値を指定します。  <br/> |Xs: 文字列型の値  <br/> |
|windspeed  <br/> |xs: 整数  <br/> |必須  <br/> |現在の数値の風向の速度の値を指定します。  <br/> |Xs: integer 型の値  <br/> |
   

