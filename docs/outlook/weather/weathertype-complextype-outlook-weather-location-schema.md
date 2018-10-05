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
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="1bfae-103">weatherType complexType (Outlook の天気予報の場所のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="1bfae-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="1bfae-104">場所の気象条件のパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="1bfae-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="1bfae-105">型情報</span><span class="sxs-lookup"><span data-stu-id="1bfae-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bfae-106">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1bfae-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="1bfae-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1bfae-107">**Schema file**</span></span> <br/> |<span data-ttu-id="1bfae-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="1bfae-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="1bfae-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="1bfae-109">**Extension base**</span></span> <br/> |<span data-ttu-id="1bfae-110">なし</span><span class="sxs-lookup"><span data-stu-id="1bfae-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1bfae-111">定義</span><span class="sxs-lookup"><span data-stu-id="1bfae-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="1bfae-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1bfae-112">Elements and attributes</span></span>

<span data-ttu-id="1bfae-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1bfae-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1bfae-114">子要素</span><span class="sxs-lookup"><span data-stu-id="1bfae-114">Child elements</span></span>

<span data-ttu-id="1bfae-115">なし。</span><span class="sxs-lookup"><span data-stu-id="1bfae-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1bfae-116">属性</span><span class="sxs-lookup"><span data-stu-id="1bfae-116">Attributes</span></span>

|<span data-ttu-id="1bfae-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="1bfae-117">**Attribute**</span></span>|<span data-ttu-id="1bfae-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1bfae-118">**Type**</span></span>|<span data-ttu-id="1bfae-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="1bfae-119">**Required**</span></span>|<span data-ttu-id="1bfae-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="1bfae-120">**Description**</span></span>|<span data-ttu-id="1bfae-121">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="1bfae-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1bfae-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="1bfae-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="1bfae-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="1bfae-123">xs:string</span></span>  <br/> |<span data-ttu-id="1bfae-124">必須</span><span class="sxs-lookup"><span data-stu-id="1bfae-124">required</span></span>  <br/> |<span data-ttu-id="1bfae-125">同じ名前の複数の場所を識別するために場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="1bfae-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="1bfae-126">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="1bfae-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="1bfae-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="1bfae-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="1bfae-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="1bfae-128">xs:string</span></span>  <br/> |<span data-ttu-id="1bfae-129">必須</span><span class="sxs-lookup"><span data-stu-id="1bfae-129">required</span></span>  <br/> |<span data-ttu-id="1bfae-130">場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="1bfae-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="1bfae-131">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="1bfae-131">A value of the type xs:string</span></span>  <br/> |
   

