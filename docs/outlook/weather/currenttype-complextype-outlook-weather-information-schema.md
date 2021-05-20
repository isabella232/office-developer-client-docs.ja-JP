---
title: currentType complexType (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: 場所の現在の気象条件に関するパラメーターを定義します。
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540988"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="453a6-103">currentType complexType (Outlook天気予報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="453a6-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="453a6-104">場所の現在の気象条件に関するパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="453a6-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="453a6-105">型情報</span><span class="sxs-lookup"><span data-stu-id="453a6-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="453a6-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="453a6-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="453a6-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="453a6-107">**Schema file**</span></span> <br/> |<span data-ttu-id="453a6-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="453a6-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="453a6-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="453a6-109">**Extension base**</span></span> <br/> |<span data-ttu-id="453a6-110">なし</span><span class="sxs-lookup"><span data-stu-id="453a6-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="453a6-111">定義</span><span class="sxs-lookup"><span data-stu-id="453a6-111">Definition</span></span>

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="453a6-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="453a6-112">Elements and attributes</span></span>

<span data-ttu-id="453a6-113">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="453a6-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="453a6-114">子要素</span><span class="sxs-lookup"><span data-stu-id="453a6-114">Child elements</span></span>

<span data-ttu-id="453a6-115">なし。</span><span class="sxs-lookup"><span data-stu-id="453a6-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="453a6-116">属性</span><span class="sxs-lookup"><span data-stu-id="453a6-116">Attributes</span></span>

|<span data-ttu-id="453a6-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="453a6-117">**Attribute**</span></span>|<span data-ttu-id="453a6-118">**型**</span><span class="sxs-lookup"><span data-stu-id="453a6-118">**Type**</span></span>|<span data-ttu-id="453a6-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="453a6-119">**Required**</span></span>|<span data-ttu-id="453a6-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="453a6-120">**Description**</span></span>|<span data-ttu-id="453a6-121">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="453a6-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="453a6-122">date</span><span class="sxs-lookup"><span data-stu-id="453a6-122">date</span></span>  <br/> |<span data-ttu-id="453a6-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="453a6-123">xs:date</span></span>  <br/> |<span data-ttu-id="453a6-124">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-124">required</span></span>  <br/> |<span data-ttu-id="453a6-125">今日の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="453a6-126">xs:date 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="453a6-127">日</span><span class="sxs-lookup"><span data-stu-id="453a6-127">day</span></span>  <br/> |<span data-ttu-id="453a6-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="453a6-128">xs:string</span></span>  <br/> |<span data-ttu-id="453a6-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="453a6-129">optional</span></span>  <br/> |<span data-ttu-id="453a6-130">予測の日を指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="453a6-131">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="453a6-132">感じが良い</span><span class="sxs-lookup"><span data-stu-id="453a6-132">feelslike</span></span>  <br/> |<span data-ttu-id="453a6-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="453a6-133">xs:integer</span></span>  <br/> |<span data-ttu-id="453a6-134">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-134">required</span></span>  <br/> |<span data-ttu-id="453a6-135">現在の天気の温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="453a6-136">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="453a6-137">湿度</span><span class="sxs-lookup"><span data-stu-id="453a6-137">humidity</span></span>  <br/> |<span data-ttu-id="453a6-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="453a6-138">xs:integer</span></span>  <br/> |<span data-ttu-id="453a6-139">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-139">required</span></span>  <br/> |<span data-ttu-id="453a6-140">現在の数値の湿度値を指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="453a6-141">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="453a6-142">オブザベーションポイント</span><span class="sxs-lookup"><span data-stu-id="453a6-142">observationpoint</span></span>  <br/> |<span data-ttu-id="453a6-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="453a6-143">xs:string</span></span>  <br/> |<span data-ttu-id="453a6-144">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-144">required</span></span>  <br/> |<span data-ttu-id="453a6-145">現在の気象情報の観測場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="453a6-146">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="453a6-147">観測時間</span><span class="sxs-lookup"><span data-stu-id="453a6-147">observationtime</span></span>  <br/> |<span data-ttu-id="453a6-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="453a6-148">xs:time</span></span>  <br/> |<span data-ttu-id="453a6-149">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-149">required</span></span>  <br/> |<span data-ttu-id="453a6-150">現在の気象情報がいつ観測されるのか指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="453a6-151">xs:time 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="453a6-152">shortday</span><span class="sxs-lookup"><span data-stu-id="453a6-152">shortday</span></span>  <br/> |<span data-ttu-id="453a6-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="453a6-153">xs:string</span></span>  <br/> |<span data-ttu-id="453a6-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="453a6-154">optional</span></span>  <br/> |<span data-ttu-id="453a6-155">省略形で日を指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="453a6-156">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="453a6-157">skycode</span><span class="sxs-lookup"><span data-stu-id="453a6-157">skycode</span></span>  <br/> |<span data-ttu-id="453a6-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="453a6-158">xs:integer</span></span>  <br/> |<span data-ttu-id="453a6-159">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-159">required</span></span>  <br/> |<span data-ttu-id="453a6-160">現在の気象条件の整数コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="453a6-161">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="453a6-162">skytext</span><span class="sxs-lookup"><span data-stu-id="453a6-162">skytext</span></span>  <br/> |<span data-ttu-id="453a6-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="453a6-163">xs:string</span></span>  <br/> |<span data-ttu-id="453a6-164">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-164">required</span></span>  <br/> |<span data-ttu-id="453a6-165">現在の気象条件を表す単語を 1 から 2 つ指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="453a6-166">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="453a6-167">温度</span><span class="sxs-lookup"><span data-stu-id="453a6-167">temperature</span></span>  <br/> |<span data-ttu-id="453a6-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="453a6-168">xs:integer</span></span>  <br/> |<span data-ttu-id="453a6-169">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-169">required</span></span>  <br/> |<span data-ttu-id="453a6-170">場所の現在の温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="453a6-171">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="453a6-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="453a6-172">winddisplay</span></span>  <br/> |<span data-ttu-id="453a6-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="453a6-173">xs:string</span></span>  <br/> |<span data-ttu-id="453a6-174">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-174">required</span></span>  <br/> |<span data-ttu-id="453a6-175">現在の風の状態を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="453a6-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="453a6-176">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="453a6-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="453a6-177">windspeed</span></span>  <br/> |<span data-ttu-id="453a6-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="453a6-178">xs:integer</span></span>  <br/> |<span data-ttu-id="453a6-179">必須</span><span class="sxs-lookup"><span data-stu-id="453a6-179">required</span></span>  <br/> |<span data-ttu-id="453a6-180">現在の風速の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="453a6-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="453a6-181">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="453a6-181">A value of the type xs:integer</span></span>  <br/> |
   

