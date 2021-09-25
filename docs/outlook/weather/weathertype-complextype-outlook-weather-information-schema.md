---
title: weatherType complexType (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: 場所の気象条件を指定します。
ms.openlocfilehash: 56d4364e521cadd9a3a7062a0caf2cb82dcbd079
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616188"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a>weatherType complexType (Outlook天気予報スキーマ)

場所の気象条件を指定します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[現在の](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |現在の気象条件を指定します。  <br/> |
|[予測](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |今日、明日、明日の次の日を含む、少なくとも 3 日先の将来の気象条件を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|属性  <br/> |xs:string  <br/> |必須  <br/> |天気予報情報のソースを指定します。  <br/> |xs:string 型の値  <br/> |
|degreetype  <br/> |xs:string  <br/> |必須出席者  <br/> |場所の温度 (摂氏など) の単位を指定します。  <br/> |C、F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |必須  <br/> |場所のイメージの URL を指定します。  <br/> |xs:string 型の値  <br/> |
|timezone  <br/> |xs:integer  <br/> |必須出席者  <br/> |GMT オフセットを指定します。  <br/> |-11 ~ 12 の値  <br/> |
|url  <br/> |xs:string  <br/> |必須  <br/> |指定した場所の天気予報情報を含む天気予報サービスの Web ページの URL を指定します。  <br/> |xs:string 型の値  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |必須出席者  <br/> |同じ名前を持つ複数の場所を区別するために使用する場所に関連付けられているコードを指定します。  <br/> |xs:string 型の値  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |必須出席者  <br/> |ドロップダウン コントロールに表示される場所の名前を指定します。  <br/> |xs:string 型の値  <br/> |
   

