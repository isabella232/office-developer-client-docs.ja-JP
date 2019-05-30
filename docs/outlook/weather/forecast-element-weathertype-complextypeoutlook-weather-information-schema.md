---
title: forecast 要素 (weatherType complexType) (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540981"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="06016-103">forecast 要素 (weatherType complexType) (Outlook 天気情報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="06016-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="06016-104">今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。</span><span class="sxs-lookup"><span data-stu-id="06016-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06016-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="06016-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06016-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="06016-106">**Element type**</span></span> <br/> |[<span data-ttu-id="06016-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="06016-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="06016-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="06016-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="06016-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="06016-109">**Schema file**</span></span> <br/> |<span data-ttu-id="06016-110">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="06016-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06016-111">定義</span><span class="sxs-lookup"><span data-stu-id="06016-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="06016-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="06016-112">Elements and attributes</span></span>

<span data-ttu-id="06016-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="06016-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="06016-114">親要素</span><span class="sxs-lookup"><span data-stu-id="06016-114">Parent elements</span></span>

|<span data-ttu-id="06016-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="06016-115">**Element**</span></span>|<span data-ttu-id="06016-116">**型**</span><span class="sxs-lookup"><span data-stu-id="06016-116">**Type**</span></span>|<span data-ttu-id="06016-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="06016-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="06016-118">天気予報</span><span class="sxs-lookup"><span data-stu-id="06016-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="06016-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="06016-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="06016-120">場所の天気予報の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="06016-121">子要素</span><span class="sxs-lookup"><span data-stu-id="06016-121">Child elements</span></span>

<span data-ttu-id="06016-122">なし。</span><span class="sxs-lookup"><span data-stu-id="06016-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06016-123">属性</span><span class="sxs-lookup"><span data-stu-id="06016-123">Attributes</span></span>

|<span data-ttu-id="06016-124">**属性**</span><span class="sxs-lookup"><span data-stu-id="06016-124">**Attribute**</span></span>|<span data-ttu-id="06016-125">**型**</span><span class="sxs-lookup"><span data-stu-id="06016-125">**Type**</span></span>|<span data-ttu-id="06016-126">**必須**</span><span class="sxs-lookup"><span data-stu-id="06016-126">**Required**</span></span>|<span data-ttu-id="06016-127">**説明**</span><span class="sxs-lookup"><span data-stu-id="06016-127">**Description**</span></span>|<span data-ttu-id="06016-128">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="06016-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="06016-129">date</span><span class="sxs-lookup"><span data-stu-id="06016-129">date</span></span>  <br/> |<span data-ttu-id="06016-130">xs: date</span><span class="sxs-lookup"><span data-stu-id="06016-130">xs:date</span></span>  <br/> |<span data-ttu-id="06016-131">必須</span><span class="sxs-lookup"><span data-stu-id="06016-131">required</span></span>  <br/> |<span data-ttu-id="06016-132">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="06016-133">Xs: date 型の値</span><span class="sxs-lookup"><span data-stu-id="06016-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="06016-134">日勤</span><span class="sxs-lookup"><span data-stu-id="06016-134">day</span></span>  <br/> |<span data-ttu-id="06016-135">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="06016-135">xs:string</span></span>  <br/> |<span data-ttu-id="06016-136">必須</span><span class="sxs-lookup"><span data-stu-id="06016-136">required</span></span>  <br/> |<span data-ttu-id="06016-137">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="06016-138">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="06016-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="06016-139">高額</span><span class="sxs-lookup"><span data-stu-id="06016-139">high</span></span>  <br/> |<span data-ttu-id="06016-140">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="06016-140">xs:integer</span></span>  <br/> |<span data-ttu-id="06016-141">必須</span><span class="sxs-lookup"><span data-stu-id="06016-141">required</span></span>  <br/> |<span data-ttu-id="06016-142">予測最高温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="06016-143">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="06016-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="06016-144">低さ</span><span class="sxs-lookup"><span data-stu-id="06016-144">low</span></span>  <br/> |<span data-ttu-id="06016-145">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="06016-145">xs:integer</span></span>  <br/> |<span data-ttu-id="06016-146">必須</span><span class="sxs-lookup"><span data-stu-id="06016-146">required</span></span>  <br/> |<span data-ttu-id="06016-147">予測される最低温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="06016-148">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="06016-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="06016-149">precip</span><span class="sxs-lookup"><span data-stu-id="06016-149">precip</span></span>  <br/> |<span data-ttu-id="06016-150">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="06016-150">xs:integer</span></span>  <br/> |<span data-ttu-id="06016-151">必須</span><span class="sxs-lookup"><span data-stu-id="06016-151">required</span></span>  <br/> |<span data-ttu-id="06016-152">降水のパーセンテージを指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="06016-153">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="06016-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="06016-154">短い日</span><span class="sxs-lookup"><span data-stu-id="06016-154">shortday</span></span>  <br/> |<span data-ttu-id="06016-155">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="06016-155">xs:string</span></span>  <br/> |<span data-ttu-id="06016-156">必須</span><span class="sxs-lookup"><span data-stu-id="06016-156">required</span></span>  <br/> |<span data-ttu-id="06016-157">日付を省略された形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="06016-158">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="06016-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="06016-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="06016-159">skycodeday</span></span>  <br/> |<span data-ttu-id="06016-160">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="06016-160">xs:integer</span></span>  <br/> |<span data-ttu-id="06016-161">必須</span><span class="sxs-lookup"><span data-stu-id="06016-161">required</span></span>  <br/> |<span data-ttu-id="06016-162">予測される条件のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="06016-163">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="06016-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="06016-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="06016-164">skytextday</span></span>  <br/> |<span data-ttu-id="06016-165">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="06016-165">xs:string</span></span>  <br/> |<span data-ttu-id="06016-166">必須</span><span class="sxs-lookup"><span data-stu-id="06016-166">required</span></span>  <br/> |<span data-ttu-id="06016-167">予測条件を説明する 1 ~ 2 単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="06016-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="06016-168">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="06016-168">A value of the type xs:string</span></span>  <br/> |
   

