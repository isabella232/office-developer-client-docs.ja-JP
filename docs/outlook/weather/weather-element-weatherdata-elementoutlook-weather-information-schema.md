---
title: 気象要素 (weatherdata 要素) (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: 場所の気象条件を指定します。
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390661"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>気象要素 (weatherdata 要素) (Outlook の気象情報のスキーマ)

場所の気象条件を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-information-schema.md) <br/> ||気象要素を定義します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[現在の](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |現在の気象条件を指定します。  <br/> |
|[予測](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |今日含めて後 3 日以上の今後の気象条件を指定する: 今日、明日、明後日。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|属性  <br/> |xs:string  <br/> |必須  <br/> |気象情報のソースを指定します。  <br/> |値の型の使用されています  <br/> |
|degreetype  <br/> |xs:string  <br/> |必須  <br/> |場所たとえば、摂氏の温度の単位を指定します。  <br/> |C、F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |必須  <br/> |場所のイメージの URL を指定します。  <br/> |値の型の使用されています  <br/> |
|タイム ゾーン  <br/> |xs:integer  <br/> |必須  <br/> |GMT オフセットを指定します。  <br/> |-11 と 12 の間の値  <br/> |
|url  <br/> |xs:string  <br/> |必須  <br/> |指定した場所の気象情報を含む気象サービスの web ページの URL を指定します。  <br/> |値の型の使用されています  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |必須  <br/> |同じ名前を持つ複数の場所を識別するために使用される場所に関連付けられているコードを指定します。  <br/> |値の型の使用されています  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |必須  <br/> |ドロップ ダウン コントロールに表示されている場所の名前を指定します。  <br/> |値の型の使用されています  <br/> |
   

