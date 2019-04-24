---
title: weatherType complexType (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: 場所の天気予報の条件を指定します。
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355042"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a>weatherType complexType (Outlook 天気情報スキーマ)

場所の天気予報の条件を指定します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo  <br/> |
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

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[現在の](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currenttype](currenttype-complextype-outlook-weather-information-schema.md) <br/> |現在の気象条件を指定します。  <br/> |
|[気象](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|帰属  <br/> |xs: 文字列  <br/> |必須  <br/> |天気情報のソースを指定します。  <br/> |xs: 文字列型の値  <br/> |
|degreetype  <br/> |xs: 文字列  <br/> |必須  <br/> |場所の温度の単位を指定します。たとえば、摂氏を指定します。  <br/> |C、F  <br/> |
|imagerelativeurl  <br/> |xs: 文字列  <br/> |必須  <br/> |場所のイメージの URL を指定します。  <br/> |xs: 文字列型の値  <br/> |
|timezone  <br/> |xs: 整数  <br/> |必須  <br/> |GMT オフセットを指定します。  <br/> |-11 から12の範囲の値  <br/> |
|url  <br/> |xs: 文字列  <br/> |必須  <br/> |指定した場所の天気情報を含む天気予報サービスの web ページの URL を指定します。  <br/> |xs: 文字列型の値  <br/> |
|weatherlocationcode  <br/> |xs: 文字列  <br/> |必須  <br/> |同じ名前を持つ複数の場所を区別するために使用される場所に関連付けられているコードを指定します。  <br/> |xs: 文字列型の値  <br/> |
|weatherlocationname  <br/> |xs: 文字列  <br/> |必須  <br/> |ドロップダウンコントロールに表示される場所の名前を指定します。  <br/> |xs: 文字列型の値  <br/> |
   

