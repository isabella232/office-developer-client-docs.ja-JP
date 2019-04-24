---
title: weather 要素 (weatherdata 要素) (Outlook Weather Location スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: 気象を報告する場所を指定します。
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355210"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="b4ca6-103">weather 要素 (weatherdata 要素) (Outlook Weather Location スキーマ)</span><span class="sxs-lookup"><span data-stu-id="b4ca6-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="b4ca6-104">気象を報告する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4ca6-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4ca6-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b4ca6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4ca6-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b4ca6-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="b4ca6-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="b4ca6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="b4ca6-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b4ca6-110">getweatherlocation</span><span class="sxs-lookup"><span data-stu-id="b4ca6-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4ca6-111">定義</span><span class="sxs-lookup"><span data-stu-id="b4ca6-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="b4ca6-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b4ca6-112">Elements and attributes</span></span>

<span data-ttu-id="b4ca6-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4ca6-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b4ca6-114">親要素</span><span class="sxs-lookup"><span data-stu-id="b4ca6-114">Parent elements</span></span>

|<span data-ttu-id="b4ca6-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-115">**Element**</span></span>|<span data-ttu-id="b4ca6-116">**型**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-116">**Type**</span></span>|<span data-ttu-id="b4ca6-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4ca6-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="b4ca6-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="b4ca6-119">天気予報の要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="b4ca6-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b4ca6-120">子要素</span><span class="sxs-lookup"><span data-stu-id="b4ca6-120">Child elements</span></span>

<span data-ttu-id="b4ca6-121">なし。</span><span class="sxs-lookup"><span data-stu-id="b4ca6-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4ca6-122">属性</span><span class="sxs-lookup"><span data-stu-id="b4ca6-122">Attributes</span></span>

|<span data-ttu-id="b4ca6-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-123">**Attribute**</span></span>|<span data-ttu-id="b4ca6-124">**型**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-124">**Type**</span></span>|<span data-ttu-id="b4ca6-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-125">**Required**</span></span>|<span data-ttu-id="b4ca6-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-126">**Description**</span></span>|<span data-ttu-id="b4ca6-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="b4ca6-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b4ca6-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="b4ca6-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="b4ca6-129">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="b4ca6-129">xs:string</span></span>  <br/> |<span data-ttu-id="b4ca6-130">必須</span><span class="sxs-lookup"><span data-stu-id="b4ca6-130">required</span></span>  <br/> |<span data-ttu-id="b4ca6-131">同じ名前の複数の場所を区別するために、場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4ca6-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="b4ca6-132">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="b4ca6-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b4ca6-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="b4ca6-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="b4ca6-134">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="b4ca6-134">xs:string</span></span>  <br/> |<span data-ttu-id="b4ca6-135">必須</span><span class="sxs-lookup"><span data-stu-id="b4ca6-135">required</span></span>  <br/> |<span data-ttu-id="b4ca6-136">場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4ca6-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="b4ca6-137">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="b4ca6-137">A value of the type xs:string</span></span>  <br/> |
   

