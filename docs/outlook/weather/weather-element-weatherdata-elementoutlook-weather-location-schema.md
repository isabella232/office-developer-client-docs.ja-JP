---
title: 気象要素 (weatherdata 要素) (Outlook の天気予報の場所のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: 天気をレポートする場所を指定します。
ms.openlocfilehash: a95e207845a9e54f5cac58b64ce85ec17b59fa22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804549"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>気象要素 (weatherdata 要素) (Outlook の天気予報の場所のスキーマ)

天気をレポートする場所を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[weatherdata](weatherdata-element-outlook-weather-location-schema.md) <br/> ||気象要素を定義します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |必須  <br/> |同じ名前の複数の場所を識別するために場所に関連付けられているコードを指定します。  <br/> |値の型の使用されています  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |必須  <br/> |場所の名前を指定します。  <br/> |値の型の使用されています  <br/> |
   

