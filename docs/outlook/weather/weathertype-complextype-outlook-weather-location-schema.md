---
title: weatherType complexType (Outlook の天気予報の場所のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: 場所の気象条件のパラメーターを定義します。
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387714"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>weatherType complexType (Outlook の天気予報の場所のスキーマ)

場所の気象条件のパラメーターを定義します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**名前空間** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherlocation.xsd  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |必須  <br/> |同じ名前の複数の場所を識別するために場所に関連付けられているコードを指定します。  <br/> |値の型の使用されています  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |必須  <br/> |場所の名前を指定します。  <br/> |値の型の使用されています  <br/> |
   

