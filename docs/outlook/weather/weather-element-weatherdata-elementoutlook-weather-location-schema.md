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
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="efd62-103">気象要素 (weatherdata 要素) (Outlook の天気予報の場所のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="efd62-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="efd62-104">天気をレポートする場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="efd62-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="efd62-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="efd62-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efd62-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="efd62-106">**Element type**</span></span> <br/> |[<span data-ttu-id="efd62-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="efd62-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="efd62-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="efd62-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="efd62-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="efd62-109">**Schema file**</span></span> <br/> |<span data-ttu-id="efd62-110">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="efd62-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="efd62-111">定義</span><span class="sxs-lookup"><span data-stu-id="efd62-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="efd62-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="efd62-112">Elements and attributes</span></span>

<span data-ttu-id="efd62-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="efd62-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="efd62-114">親要素</span><span class="sxs-lookup"><span data-stu-id="efd62-114">Parent elements</span></span>

|<span data-ttu-id="efd62-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="efd62-115">**Element**</span></span>|<span data-ttu-id="efd62-116">**型**</span><span class="sxs-lookup"><span data-stu-id="efd62-116">**Type**</span></span>|<span data-ttu-id="efd62-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="efd62-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="efd62-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="efd62-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="efd62-119">気象要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="efd62-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="efd62-120">子要素</span><span class="sxs-lookup"><span data-stu-id="efd62-120">Child elements</span></span>

<span data-ttu-id="efd62-121">なし。</span><span class="sxs-lookup"><span data-stu-id="efd62-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efd62-122">属性</span><span class="sxs-lookup"><span data-stu-id="efd62-122">Attributes</span></span>

|<span data-ttu-id="efd62-123">**属性**</span><span class="sxs-lookup"><span data-stu-id="efd62-123">**Attribute**</span></span>|<span data-ttu-id="efd62-124">**型**</span><span class="sxs-lookup"><span data-stu-id="efd62-124">**Type**</span></span>|<span data-ttu-id="efd62-125">**必須**</span><span class="sxs-lookup"><span data-stu-id="efd62-125">**Required**</span></span>|<span data-ttu-id="efd62-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="efd62-126">**Description**</span></span>|<span data-ttu-id="efd62-127">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="efd62-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="efd62-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="efd62-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="efd62-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="efd62-129">xs:string</span></span>  <br/> |<span data-ttu-id="efd62-130">必須</span><span class="sxs-lookup"><span data-stu-id="efd62-130">required</span></span>  <br/> |<span data-ttu-id="efd62-131">同じ名前の複数の場所を識別するために場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="efd62-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="efd62-132">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="efd62-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="efd62-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="efd62-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="efd62-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="efd62-134">xs:string</span></span>  <br/> |<span data-ttu-id="efd62-135">必須</span><span class="sxs-lookup"><span data-stu-id="efd62-135">required</span></span>  <br/> |<span data-ttu-id="efd62-136">場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="efd62-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="efd62-137">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="efd62-137">A value of the type xs:string</span></span>  <br/> |
   

