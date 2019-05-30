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
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539013"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="efe18-103">weather 要素 (weatherdata 要素) (Outlook Weather Location スキーマ)</span><span class="sxs-lookup"><span data-stu-id="efe18-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="efe18-104">気象を報告する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="efe18-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="efe18-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="efe18-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efe18-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="efe18-106">**Element type**</span></span> <br/> |[<span data-ttu-id="efe18-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="efe18-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="efe18-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="efe18-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="efe18-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="efe18-109">**Schema file**</span></span> <br/> |<span data-ttu-id="efe18-110">getweatherlocation</span><span class="sxs-lookup"><span data-stu-id="efe18-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="efe18-111">定義</span><span class="sxs-lookup"><span data-stu-id="efe18-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="efe18-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="efe18-112">Elements and attributes</span></span>

<span data-ttu-id="efe18-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efe18-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="efe18-114">親要素</span><span class="sxs-lookup"><span data-stu-id="efe18-114">Parent elements</span></span>

|<span data-ttu-id="efe18-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="efe18-115">**Element**</span></span>|<span data-ttu-id="efe18-116">**型**</span><span class="sxs-lookup"><span data-stu-id="efe18-116">**Type**</span></span>|<span data-ttu-id="efe18-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="efe18-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="efe18-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="efe18-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="efe18-119">天気予報の要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="efe18-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="efe18-120">子要素</span><span class="sxs-lookup"><span data-stu-id="efe18-120">Child elements</span></span>

<span data-ttu-id="efe18-121">なし。</span><span class="sxs-lookup"><span data-stu-id="efe18-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efe18-122">属性</span><span class="sxs-lookup"><span data-stu-id="efe18-122">Attributes</span></span>

|<span data-ttu-id="efe18-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="efe18-123">**Attribute**</span></span>|<span data-ttu-id="efe18-124">**型**</span><span class="sxs-lookup"><span data-stu-id="efe18-124">**Type**</span></span>|<span data-ttu-id="efe18-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="efe18-125">**Required**</span></span>|<span data-ttu-id="efe18-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="efe18-126">**Description**</span></span>|<span data-ttu-id="efe18-127">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="efe18-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="efe18-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="efe18-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="efe18-129">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="efe18-129">xs:string</span></span>  <br/> |<span data-ttu-id="efe18-130">必須</span><span class="sxs-lookup"><span data-stu-id="efe18-130">required</span></span>  <br/> |<span data-ttu-id="efe18-131">同じ名前の複数の場所を区別するために、場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="efe18-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="efe18-132">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="efe18-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="efe18-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="efe18-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="efe18-134">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="efe18-134">xs:string</span></span>  <br/> |<span data-ttu-id="efe18-135">必須</span><span class="sxs-lookup"><span data-stu-id="efe18-135">required</span></span>  <br/> |<span data-ttu-id="efe18-136">場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="efe18-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="efe18-137">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="efe18-137">A value of the type xs:string</span></span>  <br/> |
   

