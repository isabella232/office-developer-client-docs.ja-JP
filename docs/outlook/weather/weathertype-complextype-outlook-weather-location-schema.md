---
title: weatherType complexType (Outlook天気予報の場所スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: 場所の気象条件に関するパラメーターを定義します。
ms.openlocfilehash: f7d33cb018daf4ece2ba468b9ebe92b0fc7b1545
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542920"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="534eb-103">weatherType complexType (Outlook天気予報の場所スキーマ)</span><span class="sxs-lookup"><span data-stu-id="534eb-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="534eb-104">場所の気象条件に関するパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="534eb-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="534eb-105">型情報</span><span class="sxs-lookup"><span data-stu-id="534eb-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="534eb-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="534eb-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="534eb-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="534eb-107">**Schema file**</span></span> <br/> |<span data-ttu-id="534eb-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="534eb-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="534eb-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="534eb-109">**Extension base**</span></span> <br/> |<span data-ttu-id="534eb-110">なし</span><span class="sxs-lookup"><span data-stu-id="534eb-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="534eb-111">定義</span><span class="sxs-lookup"><span data-stu-id="534eb-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="534eb-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="534eb-112">Elements and attributes</span></span>

<span data-ttu-id="534eb-113">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="534eb-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="534eb-114">子要素</span><span class="sxs-lookup"><span data-stu-id="534eb-114">Child elements</span></span>

<span data-ttu-id="534eb-115">なし。</span><span class="sxs-lookup"><span data-stu-id="534eb-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="534eb-116">属性</span><span class="sxs-lookup"><span data-stu-id="534eb-116">Attributes</span></span>

|<span data-ttu-id="534eb-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="534eb-117">**Attribute**</span></span>|<span data-ttu-id="534eb-118">**型**</span><span class="sxs-lookup"><span data-stu-id="534eb-118">**Type**</span></span>|<span data-ttu-id="534eb-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="534eb-119">**Required**</span></span>|<span data-ttu-id="534eb-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="534eb-120">**Description**</span></span>|<span data-ttu-id="534eb-121">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="534eb-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="534eb-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="534eb-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="534eb-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="534eb-123">xs:string</span></span>  <br/> |<span data-ttu-id="534eb-124">必須</span><span class="sxs-lookup"><span data-stu-id="534eb-124">required</span></span>  <br/> |<span data-ttu-id="534eb-125">同じ名前の複数の場所を区別する場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="534eb-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="534eb-126">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="534eb-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="534eb-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="534eb-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="534eb-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="534eb-128">xs:string</span></span>  <br/> |<span data-ttu-id="534eb-129">必須</span><span class="sxs-lookup"><span data-stu-id="534eb-129">required</span></span>  <br/> |<span data-ttu-id="534eb-130">場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="534eb-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="534eb-131">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="534eb-131">A value of the type xs:string</span></span>  <br/> |
   

