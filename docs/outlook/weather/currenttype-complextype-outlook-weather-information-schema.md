---
title: currentType complexType (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: 場所の現在の気象条件に関するパラメーターを定義します。
ms.openlocfilehash: 55ea2cfa6904d88c695268675bc7a893fa643010
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804473"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (Outlook の気象情報のスキーマ)

場所の現在の気象条件に関するパラメーターを定義します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
|**拡張機能の基本** <br/> |なし  <br/> |
   
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

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |必須  <br/> |今日の日付を指定します。  <br/> |型 xs:date の値  <br/> |
|1 日  <br/> |xs:string  <br/> |省略可能  <br/> |予測の 1 日を指定します。  <br/> |値の型の使用されています  <br/> |
|feelslike  <br/> |xs:integer  <br/> |必須  <br/> |ように現在の天気予報の気の温度を指定します。  <br/> |型 xs:integer の値  <br/> |
|湿度  <br/> |xs:integer  <br/> |必須  <br/> |現在湿度の数値の値を指定します。  <br/> |型 xs:integer の値  <br/> |
|observationpoint  <br/> |xs:string  <br/> |必須  <br/> |現在の気象情報を確認する場所を指定します。  <br/> |値の型の使用されています  <br/> |
|observationtime  <br/> |xs:time  <br/> |必須  <br/> |現在の気象情報を確認するときを指定します。  <br/> |型 xs:time の値  <br/> |
|shortday  <br/> |xs:string  <br/> |省略可能  <br/> |省略形で 1 日を指定します。  <br/> |値の型の使用されています  <br/> |
|skycode  <br/> |xs:integer  <br/> |必須  <br/> |現在の気象条件に整数コードを指定します。  <br/> |型 xs:integer の値  <br/> |
|skytext  <br/> |xs:string  <br/> |必須  <br/> |現在の気象条件を記述する 1、2 の単語を指定します。  <br/> |値の型の使用されています  <br/> |
|温度  <br/> |xs:integer  <br/> |必須  <br/> |場所の現在の温度を指定します。  <br/> |型 xs:integer の値  <br/> |
|winddisplay  <br/> |xs:string  <br/> |必須  <br/> |現在の風の状況を説明する文字列。  <br/> |値の型の使用されています  <br/> |
|風速  <br/> |xs:integer  <br/> |必須  <br/> |現在の数値の風の速度の値を指定します。  <br/> |型 xs:integer の値  <br/> |
   

