---
title: forecastType complexType (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: 場所の天気予報天気予報に関するパラメーターを定義します。
ms.openlocfilehash: 815f7131fc4869a7015c0fee15d0e8d68d0905dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619317"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (Outlook天気予報スキーマ)

場所の天気予報天気予報に関するパラメーターを定義します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
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

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |必須  <br/> |予測の日付を指定します。  <br/> |xs:date 型の値  <br/> |
|日  <br/> |xs:string  <br/> |必須出席者  <br/> |予測の日を指定します。  <br/> |xs:string 型の値  <br/> |
|high  <br/> |xs:integer  <br/> |必須  <br/> |予測される最高温度を指定します。  <br/> |xs:integer 型の値  <br/> |
|low  <br/> |xs:integer  <br/> |必須  <br/> |予測される最低温度を指定します。  <br/> |xs:integer 型の値  <br/> |
|precip  <br/> |xs:integer  <br/> |必須  <br/> |降水の可能性の割合を指定します。  <br/> |xs:integer 型の値  <br/> |
|shortday  <br/> |xs:string  <br/> |必須出席者  <br/> |省略形で日を指定します。  <br/> |xs:string 型の値  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |必須出席者  <br/> |予測条件のコードを指定します。  <br/> |xs:integer 型の値  <br/> |
|skytextday  <br/> |xs:string  <br/> |必須出席者  <br/> |予測条件を表す 1 から 2 つの単語を指定します。  <br/> |xs:string 型の値  <br/> |
   

