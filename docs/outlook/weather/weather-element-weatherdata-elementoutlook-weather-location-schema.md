---
title: weather 要素 (weatherdata 要素) (Outlook天気予報の場所スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: 天気予報を報告する場所を指定します。
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539013"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="db9f5-103">weather 要素 (weatherdata 要素) (Outlook天気予報の場所スキーマ)</span><span class="sxs-lookup"><span data-stu-id="db9f5-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="db9f5-104">天気予報を報告する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="db9f5-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db9f5-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="db9f5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db9f5-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="db9f5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="db9f5-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="db9f5-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="db9f5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="db9f5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="db9f5-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="db9f5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="db9f5-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="db9f5-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="db9f5-111">定義</span><span class="sxs-lookup"><span data-stu-id="db9f5-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="db9f5-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="db9f5-112">Elements and attributes</span></span>

<span data-ttu-id="db9f5-113">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="db9f5-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="db9f5-114">親要素</span><span class="sxs-lookup"><span data-stu-id="db9f5-114">Parent elements</span></span>

|<span data-ttu-id="db9f5-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="db9f5-115">**Element**</span></span>|<span data-ttu-id="db9f5-116">**型**</span><span class="sxs-lookup"><span data-stu-id="db9f5-116">**Type**</span></span>|<span data-ttu-id="db9f5-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="db9f5-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="db9f5-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="db9f5-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="db9f5-119">weather 要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="db9f5-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="db9f5-120">子要素</span><span class="sxs-lookup"><span data-stu-id="db9f5-120">Child elements</span></span>

<span data-ttu-id="db9f5-121">なし。</span><span class="sxs-lookup"><span data-stu-id="db9f5-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db9f5-122">属性</span><span class="sxs-lookup"><span data-stu-id="db9f5-122">Attributes</span></span>

|<span data-ttu-id="db9f5-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="db9f5-123">**Attribute**</span></span>|<span data-ttu-id="db9f5-124">**型**</span><span class="sxs-lookup"><span data-stu-id="db9f5-124">**Type**</span></span>|<span data-ttu-id="db9f5-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="db9f5-125">**Required**</span></span>|<span data-ttu-id="db9f5-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="db9f5-126">**Description**</span></span>|<span data-ttu-id="db9f5-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="db9f5-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="db9f5-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="db9f5-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="db9f5-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="db9f5-129">xs:string</span></span>  <br/> |<span data-ttu-id="db9f5-130">必須</span><span class="sxs-lookup"><span data-stu-id="db9f5-130">required</span></span>  <br/> |<span data-ttu-id="db9f5-131">同じ名前の複数の場所を区別する場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="db9f5-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="db9f5-132">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="db9f5-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="db9f5-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="db9f5-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="db9f5-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="db9f5-134">xs:string</span></span>  <br/> |<span data-ttu-id="db9f5-135">必須</span><span class="sxs-lookup"><span data-stu-id="db9f5-135">required</span></span>  <br/> |<span data-ttu-id="db9f5-136">場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="db9f5-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="db9f5-137">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="db9f5-137">A value of the type xs:string</span></span>  <br/> |
   

