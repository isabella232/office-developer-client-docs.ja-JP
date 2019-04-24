---
title: currenttype complexType (Outlook Weather Information スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: 場所の現在の天気状況に関するパラメーターを定義します。
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338452"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="75b41-103">currenttype complexType (Outlook Weather Information スキーマ)</span><span class="sxs-lookup"><span data-stu-id="75b41-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="75b41-104">場所の現在の天気状況に関するパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="75b41-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="75b41-105">型情報</span><span class="sxs-lookup"><span data-stu-id="75b41-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75b41-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="75b41-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="75b41-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="75b41-107">**Schema file**</span></span> <br/> |<span data-ttu-id="75b41-108">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="75b41-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="75b41-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="75b41-109">**Extension base**</span></span> <br/> |<span data-ttu-id="75b41-110">なし</span><span class="sxs-lookup"><span data-stu-id="75b41-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="75b41-111">定義</span><span class="sxs-lookup"><span data-stu-id="75b41-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="75b41-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="75b41-112">Elements and attributes</span></span>

<span data-ttu-id="75b41-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="75b41-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="75b41-114">子要素</span><span class="sxs-lookup"><span data-stu-id="75b41-114">Child elements</span></span>

<span data-ttu-id="75b41-115">なし。</span><span class="sxs-lookup"><span data-stu-id="75b41-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75b41-116">属性</span><span class="sxs-lookup"><span data-stu-id="75b41-116">Attributes</span></span>

|<span data-ttu-id="75b41-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="75b41-117">**Attribute**</span></span>|<span data-ttu-id="75b41-118">**型**</span><span class="sxs-lookup"><span data-stu-id="75b41-118">**Type**</span></span>|<span data-ttu-id="75b41-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="75b41-119">**Required**</span></span>|<span data-ttu-id="75b41-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="75b41-120">**Description**</span></span>|<span data-ttu-id="75b41-121">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="75b41-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="75b41-122">日付</span><span class="sxs-lookup"><span data-stu-id="75b41-122">date</span></span>  <br/> |<span data-ttu-id="75b41-123">xs: date</span><span class="sxs-lookup"><span data-stu-id="75b41-123">xs:date</span></span>  <br/> |<span data-ttu-id="75b41-124">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-124">required</span></span>  <br/> |<span data-ttu-id="75b41-125">今日の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="75b41-126">xs: date 型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="75b41-127">日勤</span><span class="sxs-lookup"><span data-stu-id="75b41-127">day</span></span>  <br/> |<span data-ttu-id="75b41-128">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="75b41-128">xs:string</span></span>  <br/> |<span data-ttu-id="75b41-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="75b41-129">optional</span></span>  <br/> |<span data-ttu-id="75b41-130">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="75b41-131">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="75b41-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="75b41-132">feelslike</span></span>  <br/> |<span data-ttu-id="75b41-133">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="75b41-133">xs:integer</span></span>  <br/> |<span data-ttu-id="75b41-134">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-134">required</span></span>  <br/> |<span data-ttu-id="75b41-135">現在の天気予報の温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="75b41-136">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="75b41-137">湿気</span><span class="sxs-lookup"><span data-stu-id="75b41-137">humidity</span></span>  <br/> |<span data-ttu-id="75b41-138">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="75b41-138">xs:integer</span></span>  <br/> |<span data-ttu-id="75b41-139">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-139">required</span></span>  <br/> |<span data-ttu-id="75b41-140">現在の数値の湿度値を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="75b41-141">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="75b41-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="75b41-142">observationpoint</span></span>  <br/> |<span data-ttu-id="75b41-143">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="75b41-143">xs:string</span></span>  <br/> |<span data-ttu-id="75b41-144">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-144">required</span></span>  <br/> |<span data-ttu-id="75b41-145">現在の天気情報の参照先を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="75b41-146">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="75b41-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="75b41-147">observationtime</span></span>  <br/> |<span data-ttu-id="75b41-148">xs: time</span><span class="sxs-lookup"><span data-stu-id="75b41-148">xs:time</span></span>  <br/> |<span data-ttu-id="75b41-149">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-149">required</span></span>  <br/> |<span data-ttu-id="75b41-150">現在の天気予報がどのような場合に観測されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="75b41-151">xs: time 型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="75b41-152">短い日</span><span class="sxs-lookup"><span data-stu-id="75b41-152">shortday</span></span>  <br/> |<span data-ttu-id="75b41-153">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="75b41-153">xs:string</span></span>  <br/> |<span data-ttu-id="75b41-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="75b41-154">optional</span></span>  <br/> |<span data-ttu-id="75b41-155">日付を省略された形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="75b41-156">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="75b41-157">skycode</span><span class="sxs-lookup"><span data-stu-id="75b41-157">skycode</span></span>  <br/> |<span data-ttu-id="75b41-158">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="75b41-158">xs:integer</span></span>  <br/> |<span data-ttu-id="75b41-159">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-159">required</span></span>  <br/> |<span data-ttu-id="75b41-160">現在の天気予報の整数コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="75b41-161">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="75b41-162">skytext</span><span class="sxs-lookup"><span data-stu-id="75b41-162">skytext</span></span>  <br/> |<span data-ttu-id="75b41-163">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="75b41-163">xs:string</span></span>  <br/> |<span data-ttu-id="75b41-164">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-164">required</span></span>  <br/> |<span data-ttu-id="75b41-165">現在の天気状況について、1 ~ 2 個の単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="75b41-166">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="75b41-167">変化</span><span class="sxs-lookup"><span data-stu-id="75b41-167">temperature</span></span>  <br/> |<span data-ttu-id="75b41-168">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="75b41-168">xs:integer</span></span>  <br/> |<span data-ttu-id="75b41-169">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-169">required</span></span>  <br/> |<span data-ttu-id="75b41-170">場所の現在の温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="75b41-171">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="75b41-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="75b41-172">winddisplay</span></span>  <br/> |<span data-ttu-id="75b41-173">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="75b41-173">xs:string</span></span>  <br/> |<span data-ttu-id="75b41-174">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-174">required</span></span>  <br/> |<span data-ttu-id="75b41-175">現在の風向きに関する条件を表す文字列型 (string) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="75b41-176">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="75b41-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="75b41-177">windspeed</span></span>  <br/> |<span data-ttu-id="75b41-178">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="75b41-178">xs:integer</span></span>  <br/> |<span data-ttu-id="75b41-179">必須</span><span class="sxs-lookup"><span data-stu-id="75b41-179">required</span></span>  <br/> |<span data-ttu-id="75b41-180">現在の数値の風向の速度の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="75b41-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="75b41-181">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="75b41-181">A value of the type xs:integer</span></span>  <br/> |
   

