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
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339565"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="f7159-103">forecast 要素 (weatherType complexType) (Outlook 天気情報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="f7159-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="f7159-104">今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。</span><span class="sxs-lookup"><span data-stu-id="f7159-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7159-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="f7159-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7159-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="f7159-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f7159-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="f7159-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="f7159-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f7159-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="f7159-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="f7159-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f7159-110">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="f7159-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f7159-111">定義</span><span class="sxs-lookup"><span data-stu-id="f7159-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="f7159-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="f7159-112">Elements and attributes</span></span>

<span data-ttu-id="f7159-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7159-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f7159-114">親要素</span><span class="sxs-lookup"><span data-stu-id="f7159-114">Parent elements</span></span>

|<span data-ttu-id="f7159-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="f7159-115">**Element**</span></span>|<span data-ttu-id="f7159-116">**型**</span><span class="sxs-lookup"><span data-stu-id="f7159-116">**Type**</span></span>|<span data-ttu-id="f7159-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="f7159-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f7159-118">天気予報</span><span class="sxs-lookup"><span data-stu-id="f7159-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="f7159-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="f7159-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="f7159-120">場所の天気予報の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f7159-121">子要素</span><span class="sxs-lookup"><span data-stu-id="f7159-121">Child elements</span></span>

<span data-ttu-id="f7159-122">なし。</span><span class="sxs-lookup"><span data-stu-id="f7159-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7159-123">属性</span><span class="sxs-lookup"><span data-stu-id="f7159-123">Attributes</span></span>

|<span data-ttu-id="f7159-124">**属性**</span><span class="sxs-lookup"><span data-stu-id="f7159-124">**Attribute**</span></span>|<span data-ttu-id="f7159-125">**型**</span><span class="sxs-lookup"><span data-stu-id="f7159-125">**Type**</span></span>|<span data-ttu-id="f7159-126">**必須**</span><span class="sxs-lookup"><span data-stu-id="f7159-126">**Required**</span></span>|<span data-ttu-id="f7159-127">**説明**</span><span class="sxs-lookup"><span data-stu-id="f7159-127">**Description**</span></span>|<span data-ttu-id="f7159-128">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="f7159-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f7159-129">日付</span><span class="sxs-lookup"><span data-stu-id="f7159-129">date</span></span>  <br/> |<span data-ttu-id="f7159-130">xs: date</span><span class="sxs-lookup"><span data-stu-id="f7159-130">xs:date</span></span>  <br/> |<span data-ttu-id="f7159-131">必須</span><span class="sxs-lookup"><span data-stu-id="f7159-131">required</span></span>  <br/> |<span data-ttu-id="f7159-132">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="f7159-133">xs: date 型の値</span><span class="sxs-lookup"><span data-stu-id="f7159-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="f7159-134">日勤</span><span class="sxs-lookup"><span data-stu-id="f7159-134">day</span></span>  <br/> |<span data-ttu-id="f7159-135">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="f7159-135">xs:string</span></span>  <br/> |<span data-ttu-id="f7159-136">必須</span><span class="sxs-lookup"><span data-stu-id="f7159-136">required</span></span>  <br/> |<span data-ttu-id="f7159-137">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="f7159-138">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="f7159-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f7159-139">高額</span><span class="sxs-lookup"><span data-stu-id="f7159-139">high</span></span>  <br/> |<span data-ttu-id="f7159-140">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="f7159-140">xs:integer</span></span>  <br/> |<span data-ttu-id="f7159-141">必須</span><span class="sxs-lookup"><span data-stu-id="f7159-141">required</span></span>  <br/> |<span data-ttu-id="f7159-142">予測最高温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="f7159-143">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="f7159-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f7159-144">低さ</span><span class="sxs-lookup"><span data-stu-id="f7159-144">low</span></span>  <br/> |<span data-ttu-id="f7159-145">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="f7159-145">xs:integer</span></span>  <br/> |<span data-ttu-id="f7159-146">必須</span><span class="sxs-lookup"><span data-stu-id="f7159-146">required</span></span>  <br/> |<span data-ttu-id="f7159-147">予測される最低温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="f7159-148">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="f7159-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f7159-149">precip</span><span class="sxs-lookup"><span data-stu-id="f7159-149">precip</span></span>  <br/> |<span data-ttu-id="f7159-150">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="f7159-150">xs:integer</span></span>  <br/> |<span data-ttu-id="f7159-151">必須</span><span class="sxs-lookup"><span data-stu-id="f7159-151">required</span></span>  <br/> |<span data-ttu-id="f7159-152">降水のパーセンテージを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="f7159-153">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="f7159-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f7159-154">短い日</span><span class="sxs-lookup"><span data-stu-id="f7159-154">shortday</span></span>  <br/> |<span data-ttu-id="f7159-155">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="f7159-155">xs:string</span></span>  <br/> |<span data-ttu-id="f7159-156">必須</span><span class="sxs-lookup"><span data-stu-id="f7159-156">required</span></span>  <br/> |<span data-ttu-id="f7159-157">日付を省略された形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="f7159-158">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="f7159-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="f7159-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="f7159-159">skycodeday</span></span>  <br/> |<span data-ttu-id="f7159-160">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="f7159-160">xs:integer</span></span>  <br/> |<span data-ttu-id="f7159-161">必須</span><span class="sxs-lookup"><span data-stu-id="f7159-161">required</span></span>  <br/> |<span data-ttu-id="f7159-162">予測される条件のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="f7159-163">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="f7159-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="f7159-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="f7159-164">skytextday</span></span>  <br/> |<span data-ttu-id="f7159-165">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="f7159-165">xs:string</span></span>  <br/> |<span data-ttu-id="f7159-166">必須</span><span class="sxs-lookup"><span data-stu-id="f7159-166">required</span></span>  <br/> |<span data-ttu-id="f7159-167">予測条件を説明する 1 ~ 2 単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7159-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="f7159-168">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="f7159-168">A value of the type xs:string</span></span>  <br/> |
   

