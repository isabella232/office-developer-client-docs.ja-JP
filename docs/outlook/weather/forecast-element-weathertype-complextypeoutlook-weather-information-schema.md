---
title: 要素 (weatherType の複合型) を予測する (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: '今日含めて後 3 日以上の今後の気象条件を指定する: 今日、明日、明後日。'
ms.openlocfilehash: c618b753ddf8a72fce270800675982f1a7f7af5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804474"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="9e3a1-103">要素 (weatherType の複合型) を予測する (Outlook の気象情報のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="9e3a1-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="9e3a1-104">今日含めて後 3 日以上の今後の気象条件を指定する: 今日、明日、明後日。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e3a1-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="9e3a1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e3a1-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9e3a1-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="9e3a1-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="9e3a1-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="9e3a1-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9e3a1-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="9e3a1-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9e3a1-111">定義</span><span class="sxs-lookup"><span data-stu-id="9e3a1-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="9e3a1-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="9e3a1-112">Elements and attributes</span></span>

<span data-ttu-id="9e3a1-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9e3a1-114">親要素</span><span class="sxs-lookup"><span data-stu-id="9e3a1-114">Parent elements</span></span>

|<span data-ttu-id="9e3a1-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-115">**Element**</span></span>|<span data-ttu-id="9e3a1-116">**型**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-116">**Type**</span></span>|<span data-ttu-id="9e3a1-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9e3a1-118">天気</span><span class="sxs-lookup"><span data-stu-id="9e3a1-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="9e3a1-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="9e3a1-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="9e3a1-120">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9e3a1-121">子要素</span><span class="sxs-lookup"><span data-stu-id="9e3a1-121">Child elements</span></span>

<span data-ttu-id="9e3a1-122">なし。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e3a1-123">属性</span><span class="sxs-lookup"><span data-stu-id="9e3a1-123">Attributes</span></span>

|<span data-ttu-id="9e3a1-124">**属性**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-124">**Attribute**</span></span>|<span data-ttu-id="9e3a1-125">**型**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-125">**Type**</span></span>|<span data-ttu-id="9e3a1-126">**必須**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-126">**Required**</span></span>|<span data-ttu-id="9e3a1-127">**説明**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-127">**Description**</span></span>|<span data-ttu-id="9e3a1-128">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="9e3a1-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9e3a1-129">date</span><span class="sxs-lookup"><span data-stu-id="9e3a1-129">date</span></span>  <br/> |<span data-ttu-id="9e3a1-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="9e3a1-130">xs:date</span></span>  <br/> |<span data-ttu-id="9e3a1-131">必須</span><span class="sxs-lookup"><span data-stu-id="9e3a1-131">required</span></span>  <br/> |<span data-ttu-id="9e3a1-132">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="9e3a1-133">型 xs:date の値</span><span class="sxs-lookup"><span data-stu-id="9e3a1-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="9e3a1-134">1 日</span><span class="sxs-lookup"><span data-stu-id="9e3a1-134">day</span></span>  <br/> |<span data-ttu-id="9e3a1-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="9e3a1-135">xs:string</span></span>  <br/> |<span data-ttu-id="9e3a1-136">必須</span><span class="sxs-lookup"><span data-stu-id="9e3a1-136">required</span></span>  <br/> |<span data-ttu-id="9e3a1-137">予測の 1 日を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="9e3a1-138">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="9e3a1-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9e3a1-139">高</span><span class="sxs-lookup"><span data-stu-id="9e3a1-139">high</span></span>  <br/> |<span data-ttu-id="9e3a1-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9e3a1-140">xs:integer</span></span>  <br/> |<span data-ttu-id="9e3a1-141">必須</span><span class="sxs-lookup"><span data-stu-id="9e3a1-141">required</span></span>  <br/> |<span data-ttu-id="9e3a1-142">予測の最高温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="9e3a1-143">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="9e3a1-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9e3a1-144">低</span><span class="sxs-lookup"><span data-stu-id="9e3a1-144">low</span></span>  <br/> |<span data-ttu-id="9e3a1-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9e3a1-145">xs:integer</span></span>  <br/> |<span data-ttu-id="9e3a1-146">必須</span><span class="sxs-lookup"><span data-stu-id="9e3a1-146">required</span></span>  <br/> |<span data-ttu-id="9e3a1-147">予測の最低温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="9e3a1-148">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="9e3a1-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9e3a1-149">precip</span><span class="sxs-lookup"><span data-stu-id="9e3a1-149">precip</span></span>  <br/> |<span data-ttu-id="9e3a1-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9e3a1-150">xs:integer</span></span>  <br/> |<span data-ttu-id="9e3a1-151">必須</span><span class="sxs-lookup"><span data-stu-id="9e3a1-151">required</span></span>  <br/> |<span data-ttu-id="9e3a1-152">降水の発生する可能性の割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="9e3a1-153">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="9e3a1-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9e3a1-154">shortday</span><span class="sxs-lookup"><span data-stu-id="9e3a1-154">shortday</span></span>  <br/> |<span data-ttu-id="9e3a1-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="9e3a1-155">xs:string</span></span>  <br/> |<span data-ttu-id="9e3a1-156">必須</span><span class="sxs-lookup"><span data-stu-id="9e3a1-156">required</span></span>  <br/> |<span data-ttu-id="9e3a1-157">省略形で 1 日を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="9e3a1-158">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="9e3a1-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9e3a1-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="9e3a1-159">skycodeday</span></span>  <br/> |<span data-ttu-id="9e3a1-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9e3a1-160">xs:integer</span></span>  <br/> |<span data-ttu-id="9e3a1-161">必須</span><span class="sxs-lookup"><span data-stu-id="9e3a1-161">required</span></span>  <br/> |<span data-ttu-id="9e3a1-162">予測の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="9e3a1-163">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="9e3a1-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9e3a1-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="9e3a1-164">skytextday</span></span>  <br/> |<span data-ttu-id="9e3a1-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="9e3a1-165">xs:string</span></span>  <br/> |<span data-ttu-id="9e3a1-166">必須</span><span class="sxs-lookup"><span data-stu-id="9e3a1-166">required</span></span>  <br/> |<span data-ttu-id="9e3a1-167">予測の条件を説明する 1、2 語を指定します。</span><span class="sxs-lookup"><span data-stu-id="9e3a1-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="9e3a1-168">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="9e3a1-168">A value of the type xs:string</span></span>  <br/> |
   

