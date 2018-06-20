---
title: forecastType complexType (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: 場所の予測の気象条件のパラメーターを定義します。
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804468"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (Outlook の気象情報のスキーマ)

場所の予測の気象条件のパラメーターを定義します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
|**拡張機能の基本** <br/> |なし  <br/> |
   
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

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |必須  <br/> |予測の日付を指定します。  <br/> |型 xs:date の値  <br/> |
|1 日  <br/> |xs:string  <br/> |必須  <br/> |予測の 1 日を指定します。  <br/> |値の型の使用されています  <br/> |
|高  <br/> |xs:integer  <br/> |必須  <br/> |予測の最高温度を指定します。  <br/> |型 xs:integer の値  <br/> |
|低  <br/> |xs:integer  <br/> |必須  <br/> |予測の最低温度を指定します。  <br/> |型 xs:integer の値  <br/> |
|precip  <br/> |xs:integer  <br/> |必須  <br/> |降水の発生する可能性の割合を指定します。  <br/> |型 xs:integer の値  <br/> |
|shortday  <br/> |xs:string  <br/> |必須  <br/> |省略形で 1 日を指定します。  <br/> |値の型の使用されています  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |必須  <br/> |予測の条件を指定します。  <br/> |型 xs:integer の値  <br/> |
|skytextday  <br/> |xs:string  <br/> |必須  <br/> |予測の条件を説明する 1、2 語を指定します。  <br/> |値の型の使用されています  <br/> |
   

