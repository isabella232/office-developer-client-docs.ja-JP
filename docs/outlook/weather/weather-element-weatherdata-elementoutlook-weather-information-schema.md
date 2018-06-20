---
title: 気象要素 (weatherdata 要素) (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: 場所の気象条件を指定します。
ms.openlocfilehash: c19db6657860dd35f90832aef0614f4fb88d87b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804546"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="27da7-103">気象要素 (weatherdata 要素) (Outlook の気象情報のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="27da7-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="27da7-104">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27da7-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="27da7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27da7-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="27da7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="27da7-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="27da7-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="27da7-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="27da7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="27da7-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="27da7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="27da7-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="27da7-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="27da7-111">定義</span><span class="sxs-lookup"><span data-stu-id="27da7-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="27da7-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="27da7-112">Elements and attributes</span></span>

<span data-ttu-id="27da7-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27da7-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="27da7-114">親要素</span><span class="sxs-lookup"><span data-stu-id="27da7-114">Parent elements</span></span>

|<span data-ttu-id="27da7-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="27da7-115">**Element**</span></span>|<span data-ttu-id="27da7-116">**型**</span><span class="sxs-lookup"><span data-stu-id="27da7-116">**Type**</span></span>|<span data-ttu-id="27da7-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="27da7-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27da7-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="27da7-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="27da7-119">気象要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="27da7-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="27da7-120">子要素</span><span class="sxs-lookup"><span data-stu-id="27da7-120">Child elements</span></span>

|<span data-ttu-id="27da7-121">**要素**</span><span class="sxs-lookup"><span data-stu-id="27da7-121">**Element**</span></span>|<span data-ttu-id="27da7-122">**型**</span><span class="sxs-lookup"><span data-stu-id="27da7-122">**Type**</span></span>|<span data-ttu-id="27da7-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="27da7-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="27da7-124">現在の</span><span class="sxs-lookup"><span data-stu-id="27da7-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="27da7-125">currentType</span><span class="sxs-lookup"><span data-stu-id="27da7-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="27da7-126">現在の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="27da7-127">予測</span><span class="sxs-lookup"><span data-stu-id="27da7-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="27da7-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="27da7-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="27da7-129">今日含めて後 3 日以上の今後の気象条件を指定する: 今日、明日、明後日。</span><span class="sxs-lookup"><span data-stu-id="27da7-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="27da7-130">属性</span><span class="sxs-lookup"><span data-stu-id="27da7-130">Attributes</span></span>

|<span data-ttu-id="27da7-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="27da7-131">**Attribute**</span></span>|<span data-ttu-id="27da7-132">**型**</span><span class="sxs-lookup"><span data-stu-id="27da7-132">**Type**</span></span>|<span data-ttu-id="27da7-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="27da7-133">**Required**</span></span>|<span data-ttu-id="27da7-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="27da7-134">**Description**</span></span>|<span data-ttu-id="27da7-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="27da7-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="27da7-136">属性</span><span class="sxs-lookup"><span data-stu-id="27da7-136">attribution</span></span>  <br/> |<span data-ttu-id="27da7-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="27da7-137">xs:string</span></span>  <br/> |<span data-ttu-id="27da7-138">必須</span><span class="sxs-lookup"><span data-stu-id="27da7-138">required</span></span>  <br/> |<span data-ttu-id="27da7-139">気象情報のソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="27da7-140">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="27da7-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="27da7-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="27da7-141">degreetype</span></span>  <br/> |<span data-ttu-id="27da7-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="27da7-142">xs:string</span></span>  <br/> |<span data-ttu-id="27da7-143">必須</span><span class="sxs-lookup"><span data-stu-id="27da7-143">required</span></span>  <br/> |<span data-ttu-id="27da7-144">場所たとえば、摂氏の温度の単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="27da7-145">C、F</span><span class="sxs-lookup"><span data-stu-id="27da7-145">C, F</span></span>  <br/> |
|<span data-ttu-id="27da7-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="27da7-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="27da7-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="27da7-147">xs:string</span></span>  <br/> |<span data-ttu-id="27da7-148">必須</span><span class="sxs-lookup"><span data-stu-id="27da7-148">required</span></span>  <br/> |<span data-ttu-id="27da7-149">場所のイメージの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="27da7-150">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="27da7-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="27da7-151">タイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="27da7-151">timezone</span></span>  <br/> |<span data-ttu-id="27da7-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="27da7-152">xs:integer</span></span>  <br/> |<span data-ttu-id="27da7-153">必須</span><span class="sxs-lookup"><span data-stu-id="27da7-153">required</span></span>  <br/> |<span data-ttu-id="27da7-154">GMT オフセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="27da7-155">-11 と 12 の間の値</span><span class="sxs-lookup"><span data-stu-id="27da7-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="27da7-156">url</span><span class="sxs-lookup"><span data-stu-id="27da7-156">url</span></span>  <br/> |<span data-ttu-id="27da7-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="27da7-157">xs:string</span></span>  <br/> |<span data-ttu-id="27da7-158">必須</span><span class="sxs-lookup"><span data-stu-id="27da7-158">required</span></span>  <br/> |<span data-ttu-id="27da7-159">指定した場所の気象情報を含む気象サービスの web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="27da7-160">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="27da7-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="27da7-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="27da7-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="27da7-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="27da7-162">xs:string</span></span>  <br/> |<span data-ttu-id="27da7-163">必須</span><span class="sxs-lookup"><span data-stu-id="27da7-163">required</span></span>  <br/> |<span data-ttu-id="27da7-164">同じ名前を持つ複数の場所を識別するために使用される場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="27da7-165">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="27da7-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="27da7-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="27da7-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="27da7-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="27da7-167">xs:string</span></span>  <br/> |<span data-ttu-id="27da7-168">必須</span><span class="sxs-lookup"><span data-stu-id="27da7-168">required</span></span>  <br/> |<span data-ttu-id="27da7-169">ドロップ ダウン コントロールに表示されている場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="27da7-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="27da7-170">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="27da7-170">A value of the type xs:string</span></span>  <br/> |
   

