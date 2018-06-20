---
title: 現在の要素 (weatherType の複合型) (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: 現在の気象条件を指定します。
ms.openlocfilehash: 12265c463f0f1bba15c9bf1723cbbea6c505dba9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804467"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>現在の要素 (weatherType の複合型) (Outlook の気象情報のスキーマ)

現在の気象条件を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="current"      type="currentType">
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
   

