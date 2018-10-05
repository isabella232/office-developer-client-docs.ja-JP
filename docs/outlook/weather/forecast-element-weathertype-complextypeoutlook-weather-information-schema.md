---
title: 要素 (weatherType の複合型) を予測する (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: '今日含めて後 3 日以上の今後の気象条件を指定する: 今日、明日、明後日。'
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398326"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>要素 (weatherType の複合型) を予測する (Outlook の気象情報のスキーマ)

今日含めて後 3 日以上の今後の気象条件を指定する: 今日、明日、明後日。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[天気](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |場所の気象条件を指定します。  <br/> |
   
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
   

