---
title: forecastType complexType (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: 場所の天気予報の条件に関するパラメーターを定義します。
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540953"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (Outlook 天気情報スキーマ)

場所の天気予報の条件に関するパラメーターを定義します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo  <br/> |
|**拡張ベース** <br/> |None  <br/> |
   
## <a name="definition"></a>定義

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
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
   

