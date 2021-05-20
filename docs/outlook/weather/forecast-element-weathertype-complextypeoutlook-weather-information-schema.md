---
title: forecast 要素 (weatherType complexType) (Outlook 天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 今日、明日、明日の次の日を含む、少なくとも 3 日先の将来の気象条件を指定します。
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540981"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="8a796-103">forecast 要素 (weatherType complexType) (Outlook 天気予報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="8a796-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="8a796-104">今日、明日、明日の次の日を含む、少なくとも 3 日先の将来の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a796-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="8a796-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a796-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8a796-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8a796-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="8a796-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="8a796-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8a796-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="8a796-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8a796-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8a796-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="8a796-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8a796-111">定義</span><span class="sxs-lookup"><span data-stu-id="8a796-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="8a796-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8a796-112">Elements and attributes</span></span>

<span data-ttu-id="8a796-113">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a796-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8a796-114">親要素</span><span class="sxs-lookup"><span data-stu-id="8a796-114">Parent elements</span></span>

|<span data-ttu-id="8a796-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="8a796-115">**Element**</span></span>|<span data-ttu-id="8a796-116">**型**</span><span class="sxs-lookup"><span data-stu-id="8a796-116">**Type**</span></span>|<span data-ttu-id="8a796-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="8a796-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8a796-118">天気</span><span class="sxs-lookup"><span data-stu-id="8a796-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="8a796-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="8a796-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="8a796-120">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8a796-121">子要素</span><span class="sxs-lookup"><span data-stu-id="8a796-121">Child elements</span></span>

<span data-ttu-id="8a796-122">なし。</span><span class="sxs-lookup"><span data-stu-id="8a796-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a796-123">属性</span><span class="sxs-lookup"><span data-stu-id="8a796-123">Attributes</span></span>

|<span data-ttu-id="8a796-124">**属性**</span><span class="sxs-lookup"><span data-stu-id="8a796-124">**Attribute**</span></span>|<span data-ttu-id="8a796-125">**型**</span><span class="sxs-lookup"><span data-stu-id="8a796-125">**Type**</span></span>|<span data-ttu-id="8a796-126">**必須**</span><span class="sxs-lookup"><span data-stu-id="8a796-126">**Required**</span></span>|<span data-ttu-id="8a796-127">**説明**</span><span class="sxs-lookup"><span data-stu-id="8a796-127">**Description**</span></span>|<span data-ttu-id="8a796-128">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="8a796-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8a796-129">date</span><span class="sxs-lookup"><span data-stu-id="8a796-129">date</span></span>  <br/> |<span data-ttu-id="8a796-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="8a796-130">xs:date</span></span>  <br/> |<span data-ttu-id="8a796-131">必須</span><span class="sxs-lookup"><span data-stu-id="8a796-131">required</span></span>  <br/> |<span data-ttu-id="8a796-132">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="8a796-133">xs:date 型の値</span><span class="sxs-lookup"><span data-stu-id="8a796-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="8a796-134">日</span><span class="sxs-lookup"><span data-stu-id="8a796-134">day</span></span>  <br/> |<span data-ttu-id="8a796-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="8a796-135">xs:string</span></span>  <br/> |<span data-ttu-id="8a796-136">必須</span><span class="sxs-lookup"><span data-stu-id="8a796-136">required</span></span>  <br/> |<span data-ttu-id="8a796-137">予測の日を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="8a796-138">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="8a796-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="8a796-139">high</span><span class="sxs-lookup"><span data-stu-id="8a796-139">high</span></span>  <br/> |<span data-ttu-id="8a796-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8a796-140">xs:integer</span></span>  <br/> |<span data-ttu-id="8a796-141">必須</span><span class="sxs-lookup"><span data-stu-id="8a796-141">required</span></span>  <br/> |<span data-ttu-id="8a796-142">予測される最高温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="8a796-143">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="8a796-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="8a796-144">low</span><span class="sxs-lookup"><span data-stu-id="8a796-144">low</span></span>  <br/> |<span data-ttu-id="8a796-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8a796-145">xs:integer</span></span>  <br/> |<span data-ttu-id="8a796-146">必須</span><span class="sxs-lookup"><span data-stu-id="8a796-146">required</span></span>  <br/> |<span data-ttu-id="8a796-147">予測される最低温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="8a796-148">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="8a796-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="8a796-149">precip</span><span class="sxs-lookup"><span data-stu-id="8a796-149">precip</span></span>  <br/> |<span data-ttu-id="8a796-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8a796-150">xs:integer</span></span>  <br/> |<span data-ttu-id="8a796-151">必須</span><span class="sxs-lookup"><span data-stu-id="8a796-151">required</span></span>  <br/> |<span data-ttu-id="8a796-152">降水の可能性の割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="8a796-153">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="8a796-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="8a796-154">shortday</span><span class="sxs-lookup"><span data-stu-id="8a796-154">shortday</span></span>  <br/> |<span data-ttu-id="8a796-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="8a796-155">xs:string</span></span>  <br/> |<span data-ttu-id="8a796-156">必須</span><span class="sxs-lookup"><span data-stu-id="8a796-156">required</span></span>  <br/> |<span data-ttu-id="8a796-157">省略形で日を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="8a796-158">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="8a796-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="8a796-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="8a796-159">skycodeday</span></span>  <br/> |<span data-ttu-id="8a796-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8a796-160">xs:integer</span></span>  <br/> |<span data-ttu-id="8a796-161">必須</span><span class="sxs-lookup"><span data-stu-id="8a796-161">required</span></span>  <br/> |<span data-ttu-id="8a796-162">予測条件のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="8a796-163">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="8a796-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="8a796-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="8a796-164">skytextday</span></span>  <br/> |<span data-ttu-id="8a796-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="8a796-165">xs:string</span></span>  <br/> |<span data-ttu-id="8a796-166">必須</span><span class="sxs-lookup"><span data-stu-id="8a796-166">required</span></span>  <br/> |<span data-ttu-id="8a796-167">予測条件を表す 1 から 2 つの単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a796-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="8a796-168">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="8a796-168">A value of the type xs:string</span></span>  <br/> |
   

