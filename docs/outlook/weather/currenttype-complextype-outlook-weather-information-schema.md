---
title: currentType complexType (Outlook Weather Information スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: 場所の現在の天気状況に関するパラメーターを定義します。
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540988"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="d5ef3-103">currentType complexType (Outlook Weather Information スキーマ)</span><span class="sxs-lookup"><span data-stu-id="d5ef3-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="d5ef3-104">場所の現在の天気状況に関するパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="d5ef3-105">型情報</span><span class="sxs-lookup"><span data-stu-id="d5ef3-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5ef3-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d5ef3-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="d5ef3-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="d5ef3-107">**Schema file**</span></span> <br/> |<span data-ttu-id="d5ef3-108">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="d5ef3-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="d5ef3-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="d5ef3-109">**Extension base**</span></span> <br/> |<span data-ttu-id="d5ef3-110">None</span><span class="sxs-lookup"><span data-stu-id="d5ef3-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5ef3-111">定義</span><span class="sxs-lookup"><span data-stu-id="d5ef3-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d5ef3-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="d5ef3-112">Elements and attributes</span></span>

<span data-ttu-id="d5ef3-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5ef3-114">子要素</span><span class="sxs-lookup"><span data-stu-id="d5ef3-114">Child elements</span></span>

<span data-ttu-id="d5ef3-115">なし。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5ef3-116">属性</span><span class="sxs-lookup"><span data-stu-id="d5ef3-116">Attributes</span></span>

|<span data-ttu-id="d5ef3-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="d5ef3-117">**Attribute**</span></span>|<span data-ttu-id="d5ef3-118">**型**</span><span class="sxs-lookup"><span data-stu-id="d5ef3-118">**Type**</span></span>|<span data-ttu-id="d5ef3-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="d5ef3-119">**Required**</span></span>|<span data-ttu-id="d5ef3-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5ef3-120">**Description**</span></span>|<span data-ttu-id="d5ef3-121">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="d5ef3-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5ef3-122">date</span><span class="sxs-lookup"><span data-stu-id="d5ef3-122">date</span></span>  <br/> |<span data-ttu-id="d5ef3-123">xs: date</span><span class="sxs-lookup"><span data-stu-id="d5ef3-123">xs:date</span></span>  <br/> |<span data-ttu-id="d5ef3-124">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-124">required</span></span>  <br/> |<span data-ttu-id="d5ef3-125">今日の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="d5ef3-126">Xs: date 型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="d5ef3-127">日勤</span><span class="sxs-lookup"><span data-stu-id="d5ef3-127">day</span></span>  <br/> |<span data-ttu-id="d5ef3-128">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="d5ef3-128">xs:string</span></span>  <br/> |<span data-ttu-id="d5ef3-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5ef3-129">optional</span></span>  <br/> |<span data-ttu-id="d5ef3-130">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="d5ef3-131">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d5ef3-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="d5ef3-132">feelslike</span></span>  <br/> |<span data-ttu-id="d5ef3-133">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="d5ef3-133">xs:integer</span></span>  <br/> |<span data-ttu-id="d5ef3-134">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-134">required</span></span>  <br/> |<span data-ttu-id="d5ef3-135">現在の天気予報の温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="d5ef3-136">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d5ef3-137">湿気</span><span class="sxs-lookup"><span data-stu-id="d5ef3-137">humidity</span></span>  <br/> |<span data-ttu-id="d5ef3-138">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="d5ef3-138">xs:integer</span></span>  <br/> |<span data-ttu-id="d5ef3-139">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-139">required</span></span>  <br/> |<span data-ttu-id="d5ef3-140">現在の数値の湿度値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="d5ef3-141">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d5ef3-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="d5ef3-142">observationpoint</span></span>  <br/> |<span data-ttu-id="d5ef3-143">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="d5ef3-143">xs:string</span></span>  <br/> |<span data-ttu-id="d5ef3-144">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-144">required</span></span>  <br/> |<span data-ttu-id="d5ef3-145">現在の天気情報の参照先を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="d5ef3-146">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d5ef3-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="d5ef3-147">observationtime</span></span>  <br/> |<span data-ttu-id="d5ef3-148">xs: time</span><span class="sxs-lookup"><span data-stu-id="d5ef3-148">xs:time</span></span>  <br/> |<span data-ttu-id="d5ef3-149">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-149">required</span></span>  <br/> |<span data-ttu-id="d5ef3-150">現在の天気予報がどのような場合に観測されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="d5ef3-151">Xs: time 型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="d5ef3-152">短い日</span><span class="sxs-lookup"><span data-stu-id="d5ef3-152">shortday</span></span>  <br/> |<span data-ttu-id="d5ef3-153">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="d5ef3-153">xs:string</span></span>  <br/> |<span data-ttu-id="d5ef3-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="d5ef3-154">optional</span></span>  <br/> |<span data-ttu-id="d5ef3-155">日付を省略された形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="d5ef3-156">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d5ef3-157">skycode</span><span class="sxs-lookup"><span data-stu-id="d5ef3-157">skycode</span></span>  <br/> |<span data-ttu-id="d5ef3-158">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="d5ef3-158">xs:integer</span></span>  <br/> |<span data-ttu-id="d5ef3-159">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-159">required</span></span>  <br/> |<span data-ttu-id="d5ef3-160">現在の天気予報の整数コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="d5ef3-161">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d5ef3-162">skytext</span><span class="sxs-lookup"><span data-stu-id="d5ef3-162">skytext</span></span>  <br/> |<span data-ttu-id="d5ef3-163">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="d5ef3-163">xs:string</span></span>  <br/> |<span data-ttu-id="d5ef3-164">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-164">required</span></span>  <br/> |<span data-ttu-id="d5ef3-165">現在の天気状況について、1 ~ 2 個の単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="d5ef3-166">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d5ef3-167">変化</span><span class="sxs-lookup"><span data-stu-id="d5ef3-167">temperature</span></span>  <br/> |<span data-ttu-id="d5ef3-168">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="d5ef3-168">xs:integer</span></span>  <br/> |<span data-ttu-id="d5ef3-169">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-169">required</span></span>  <br/> |<span data-ttu-id="d5ef3-170">場所の現在の温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="d5ef3-171">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d5ef3-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="d5ef3-172">winddisplay</span></span>  <br/> |<span data-ttu-id="d5ef3-173">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="d5ef3-173">xs:string</span></span>  <br/> |<span data-ttu-id="d5ef3-174">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-174">required</span></span>  <br/> |<span data-ttu-id="d5ef3-175">現在の風向きに関する条件を表す文字列型 (string) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="d5ef3-176">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d5ef3-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="d5ef3-177">windspeed</span></span>  <br/> |<span data-ttu-id="d5ef3-178">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="d5ef3-178">xs:integer</span></span>  <br/> |<span data-ttu-id="d5ef3-179">必須</span><span class="sxs-lookup"><span data-stu-id="d5ef3-179">required</span></span>  <br/> |<span data-ttu-id="d5ef3-180">現在の数値の風向の速度の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5ef3-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="d5ef3-181">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="d5ef3-181">A value of the type xs:integer</span></span>  <br/> |
   

