---
title: weatherType complexType (Outlook Weather Location スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: 場所の天気予報のパラメーターを定義します。
ms.openlocfilehash: f7d33cb018daf4ece2ba468b9ebe92b0fc7b1545
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542920"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>weatherType complexType (Outlook Weather Location スキーマ)

場所の天気予報のパラメーターを定義します。
  
## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**スキーマ ファイル** <br/> |getweatherlocation  <br/> |
|**拡張ベース** <br/> |None  <br/> |
   
## <a name="definition"></a>定義

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs: 文字列  <br/> |必須  <br/> |同じ名前の複数の場所を区別するために、場所に関連付けられているコードを指定します。  <br/> |Xs: 文字列型の値  <br/> |
|weatherlocationname  <br/> |xs: 文字列  <br/> |必須  <br/> |場所の名前を指定します。  <br/> |Xs: 文字列型の値  <br/> |
   

