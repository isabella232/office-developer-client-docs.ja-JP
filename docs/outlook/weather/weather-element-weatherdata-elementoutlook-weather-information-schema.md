---
title: weather 要素 (weatherdata 要素) (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: 場所の気象条件を指定します。
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541268"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="b4d25-103">weather 要素 (weatherdata 要素) (Outlook天気予報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="b4d25-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="b4d25-104">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4d25-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="b4d25-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4d25-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="b4d25-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b4d25-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="b4d25-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="b4d25-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b4d25-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="b4d25-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b4d25-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b4d25-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="b4d25-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4d25-111">定義</span><span class="sxs-lookup"><span data-stu-id="b4d25-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="b4d25-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b4d25-112">Elements and attributes</span></span>

<span data-ttu-id="b4d25-113">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4d25-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b4d25-114">親要素</span><span class="sxs-lookup"><span data-stu-id="b4d25-114">Parent elements</span></span>

|<span data-ttu-id="b4d25-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="b4d25-115">**Element**</span></span>|<span data-ttu-id="b4d25-116">**型**</span><span class="sxs-lookup"><span data-stu-id="b4d25-116">**Type**</span></span>|<span data-ttu-id="b4d25-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="b4d25-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4d25-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="b4d25-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="b4d25-119">weather 要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b4d25-120">子要素</span><span class="sxs-lookup"><span data-stu-id="b4d25-120">Child elements</span></span>

|<span data-ttu-id="b4d25-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="b4d25-121">**Element**</span></span>|<span data-ttu-id="b4d25-122">**型**</span><span class="sxs-lookup"><span data-stu-id="b4d25-122">**Type**</span></span>|<span data-ttu-id="b4d25-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="b4d25-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4d25-124">現在の</span><span class="sxs-lookup"><span data-stu-id="b4d25-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="b4d25-125">currentType</span><span class="sxs-lookup"><span data-stu-id="b4d25-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="b4d25-126">現在の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="b4d25-127">予測</span><span class="sxs-lookup"><span data-stu-id="b4d25-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="b4d25-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="b4d25-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="b4d25-129">今日、明日、明日の次の日を含む、少なくとも 3 日先の将来の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b4d25-130">属性</span><span class="sxs-lookup"><span data-stu-id="b4d25-130">Attributes</span></span>

|<span data-ttu-id="b4d25-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="b4d25-131">**Attribute**</span></span>|<span data-ttu-id="b4d25-132">**型**</span><span class="sxs-lookup"><span data-stu-id="b4d25-132">**Type**</span></span>|<span data-ttu-id="b4d25-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="b4d25-133">**Required**</span></span>|<span data-ttu-id="b4d25-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="b4d25-134">**Description**</span></span>|<span data-ttu-id="b4d25-135">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="b4d25-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b4d25-136">属性</span><span class="sxs-lookup"><span data-stu-id="b4d25-136">attribution</span></span>  <br/> |<span data-ttu-id="b4d25-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d25-137">xs:string</span></span>  <br/> |<span data-ttu-id="b4d25-138">必須</span><span class="sxs-lookup"><span data-stu-id="b4d25-138">required</span></span>  <br/> |<span data-ttu-id="b4d25-139">天気予報情報のソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="b4d25-140">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="b4d25-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b4d25-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="b4d25-141">degreetype</span></span>  <br/> |<span data-ttu-id="b4d25-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d25-142">xs:string</span></span>  <br/> |<span data-ttu-id="b4d25-143">必須</span><span class="sxs-lookup"><span data-stu-id="b4d25-143">required</span></span>  <br/> |<span data-ttu-id="b4d25-144">場所の温度 (摂氏など) の単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="b4d25-145">C、F</span><span class="sxs-lookup"><span data-stu-id="b4d25-145">C, F</span></span>  <br/> |
|<span data-ttu-id="b4d25-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="b4d25-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="b4d25-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d25-147">xs:string</span></span>  <br/> |<span data-ttu-id="b4d25-148">必須</span><span class="sxs-lookup"><span data-stu-id="b4d25-148">required</span></span>  <br/> |<span data-ttu-id="b4d25-149">場所のイメージの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="b4d25-150">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="b4d25-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b4d25-151">timezone</span><span class="sxs-lookup"><span data-stu-id="b4d25-151">timezone</span></span>  <br/> |<span data-ttu-id="b4d25-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="b4d25-152">xs:integer</span></span>  <br/> |<span data-ttu-id="b4d25-153">必須</span><span class="sxs-lookup"><span data-stu-id="b4d25-153">required</span></span>  <br/> |<span data-ttu-id="b4d25-154">GMT オフセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="b4d25-155">-11 ~ 12 の値</span><span class="sxs-lookup"><span data-stu-id="b4d25-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="b4d25-156">url</span><span class="sxs-lookup"><span data-stu-id="b4d25-156">url</span></span>  <br/> |<span data-ttu-id="b4d25-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d25-157">xs:string</span></span>  <br/> |<span data-ttu-id="b4d25-158">必須</span><span class="sxs-lookup"><span data-stu-id="b4d25-158">required</span></span>  <br/> |<span data-ttu-id="b4d25-159">指定した場所の天気予報情報を含む天気予報サービスの Web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="b4d25-160">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="b4d25-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b4d25-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="b4d25-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="b4d25-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d25-162">xs:string</span></span>  <br/> |<span data-ttu-id="b4d25-163">必須</span><span class="sxs-lookup"><span data-stu-id="b4d25-163">required</span></span>  <br/> |<span data-ttu-id="b4d25-164">同じ名前を持つ複数の場所を区別するために使用する場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="b4d25-165">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="b4d25-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="b4d25-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="b4d25-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="b4d25-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="b4d25-167">xs:string</span></span>  <br/> |<span data-ttu-id="b4d25-168">必須</span><span class="sxs-lookup"><span data-stu-id="b4d25-168">required</span></span>  <br/> |<span data-ttu-id="b4d25-169">ドロップダウン コントロールに表示される場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="b4d25-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="b4d25-170">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="b4d25-170">A value of the type xs:string</span></span>  <br/> |
   

