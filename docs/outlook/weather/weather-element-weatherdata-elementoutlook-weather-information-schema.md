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
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390661"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="77e65-103">気象要素 (weatherdata 要素) (Outlook の気象情報のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="77e65-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="77e65-104">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77e65-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="77e65-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77e65-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="77e65-106">**Element type**</span></span> <br/> |[<span data-ttu-id="77e65-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="77e65-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="77e65-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="77e65-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="77e65-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="77e65-109">**Schema file**</span></span> <br/> |<span data-ttu-id="77e65-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="77e65-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="77e65-111">定義</span><span class="sxs-lookup"><span data-stu-id="77e65-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="77e65-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="77e65-112">Elements and attributes</span></span>

<span data-ttu-id="77e65-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77e65-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="77e65-114">親要素</span><span class="sxs-lookup"><span data-stu-id="77e65-114">Parent elements</span></span>

|<span data-ttu-id="77e65-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="77e65-115">**Element**</span></span>|<span data-ttu-id="77e65-116">**型**</span><span class="sxs-lookup"><span data-stu-id="77e65-116">**Type**</span></span>|<span data-ttu-id="77e65-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="77e65-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="77e65-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="77e65-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="77e65-119">気象要素を定義します。</span><span class="sxs-lookup"><span data-stu-id="77e65-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="77e65-120">子要素</span><span class="sxs-lookup"><span data-stu-id="77e65-120">Child elements</span></span>

|<span data-ttu-id="77e65-121">**要素**</span><span class="sxs-lookup"><span data-stu-id="77e65-121">**Element**</span></span>|<span data-ttu-id="77e65-122">**型**</span><span class="sxs-lookup"><span data-stu-id="77e65-122">**Type**</span></span>|<span data-ttu-id="77e65-123">**説明**</span><span class="sxs-lookup"><span data-stu-id="77e65-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="77e65-124">現在の</span><span class="sxs-lookup"><span data-stu-id="77e65-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="77e65-125">currentType</span><span class="sxs-lookup"><span data-stu-id="77e65-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="77e65-126">現在の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="77e65-127">予測</span><span class="sxs-lookup"><span data-stu-id="77e65-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="77e65-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="77e65-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="77e65-129">今日含めて後 3 日以上の今後の気象条件を指定する: 今日、明日、明後日。</span><span class="sxs-lookup"><span data-stu-id="77e65-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="77e65-130">属性</span><span class="sxs-lookup"><span data-stu-id="77e65-130">Attributes</span></span>

|<span data-ttu-id="77e65-131">**属性**</span><span class="sxs-lookup"><span data-stu-id="77e65-131">**Attribute**</span></span>|<span data-ttu-id="77e65-132">**型**</span><span class="sxs-lookup"><span data-stu-id="77e65-132">**Type**</span></span>|<span data-ttu-id="77e65-133">**必須**</span><span class="sxs-lookup"><span data-stu-id="77e65-133">**Required**</span></span>|<span data-ttu-id="77e65-134">**説明**</span><span class="sxs-lookup"><span data-stu-id="77e65-134">**Description**</span></span>|<span data-ttu-id="77e65-135">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="77e65-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="77e65-136">属性</span><span class="sxs-lookup"><span data-stu-id="77e65-136">attribution</span></span>  <br/> |<span data-ttu-id="77e65-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="77e65-137">xs:string</span></span>  <br/> |<span data-ttu-id="77e65-138">必須</span><span class="sxs-lookup"><span data-stu-id="77e65-138">required</span></span>  <br/> |<span data-ttu-id="77e65-139">気象情報のソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="77e65-140">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="77e65-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="77e65-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="77e65-141">degreetype</span></span>  <br/> |<span data-ttu-id="77e65-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="77e65-142">xs:string</span></span>  <br/> |<span data-ttu-id="77e65-143">必須</span><span class="sxs-lookup"><span data-stu-id="77e65-143">required</span></span>  <br/> |<span data-ttu-id="77e65-144">場所たとえば、摂氏の温度の単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="77e65-145">C、F</span><span class="sxs-lookup"><span data-stu-id="77e65-145">C, F</span></span>  <br/> |
|<span data-ttu-id="77e65-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="77e65-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="77e65-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="77e65-147">xs:string</span></span>  <br/> |<span data-ttu-id="77e65-148">必須</span><span class="sxs-lookup"><span data-stu-id="77e65-148">required</span></span>  <br/> |<span data-ttu-id="77e65-149">場所のイメージの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="77e65-150">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="77e65-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="77e65-151">タイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="77e65-151">timezone</span></span>  <br/> |<span data-ttu-id="77e65-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="77e65-152">xs:integer</span></span>  <br/> |<span data-ttu-id="77e65-153">必須</span><span class="sxs-lookup"><span data-stu-id="77e65-153">required</span></span>  <br/> |<span data-ttu-id="77e65-154">GMT オフセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="77e65-155">-11 と 12 の間の値</span><span class="sxs-lookup"><span data-stu-id="77e65-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="77e65-156">url</span><span class="sxs-lookup"><span data-stu-id="77e65-156">url</span></span>  <br/> |<span data-ttu-id="77e65-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="77e65-157">xs:string</span></span>  <br/> |<span data-ttu-id="77e65-158">必須</span><span class="sxs-lookup"><span data-stu-id="77e65-158">required</span></span>  <br/> |<span data-ttu-id="77e65-159">指定した場所の気象情報を含む気象サービスの web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="77e65-160">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="77e65-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="77e65-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="77e65-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="77e65-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="77e65-162">xs:string</span></span>  <br/> |<span data-ttu-id="77e65-163">必須</span><span class="sxs-lookup"><span data-stu-id="77e65-163">required</span></span>  <br/> |<span data-ttu-id="77e65-164">同じ名前を持つ複数の場所を識別するために使用される場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="77e65-165">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="77e65-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="77e65-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="77e65-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="77e65-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="77e65-167">xs:string</span></span>  <br/> |<span data-ttu-id="77e65-168">必須</span><span class="sxs-lookup"><span data-stu-id="77e65-168">required</span></span>  <br/> |<span data-ttu-id="77e65-169">ドロップ ダウン コントロールに表示されている場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="77e65-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="77e65-170">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="77e65-170">A value of the type xs:string</span></span>  <br/> |
   

