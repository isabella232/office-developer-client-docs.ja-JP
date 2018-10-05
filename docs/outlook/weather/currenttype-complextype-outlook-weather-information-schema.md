---
title: currentType complexType (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: 場所の現在の気象条件に関するパラメーターを定義します。
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387035"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="4875e-103">currentType complexType (Outlook の気象情報のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="4875e-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="4875e-104">場所の現在の気象条件に関するパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="4875e-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="4875e-105">型情報</span><span class="sxs-lookup"><span data-stu-id="4875e-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4875e-106">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="4875e-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="4875e-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4875e-107">**Schema file**</span></span> <br/> |<span data-ttu-id="4875e-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="4875e-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="4875e-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="4875e-109">**Extension base**</span></span> <br/> |<span data-ttu-id="4875e-110">なし</span><span class="sxs-lookup"><span data-stu-id="4875e-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4875e-111">定義</span><span class="sxs-lookup"><span data-stu-id="4875e-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4875e-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4875e-112">Elements and attributes</span></span>

<span data-ttu-id="4875e-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4875e-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4875e-114">子要素</span><span class="sxs-lookup"><span data-stu-id="4875e-114">Child elements</span></span>

<span data-ttu-id="4875e-115">なし。</span><span class="sxs-lookup"><span data-stu-id="4875e-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4875e-116">属性</span><span class="sxs-lookup"><span data-stu-id="4875e-116">Attributes</span></span>

|<span data-ttu-id="4875e-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="4875e-117">**Attribute**</span></span>|<span data-ttu-id="4875e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4875e-118">**Type**</span></span>|<span data-ttu-id="4875e-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="4875e-119">**Required**</span></span>|<span data-ttu-id="4875e-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="4875e-120">**Description**</span></span>|<span data-ttu-id="4875e-121">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="4875e-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4875e-122">date</span><span class="sxs-lookup"><span data-stu-id="4875e-122">date</span></span>  <br/> |<span data-ttu-id="4875e-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="4875e-123">xs:date</span></span>  <br/> |<span data-ttu-id="4875e-124">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-124">required</span></span>  <br/> |<span data-ttu-id="4875e-125">今日の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="4875e-126">型 xs:date の値</span><span class="sxs-lookup"><span data-stu-id="4875e-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="4875e-127">1 日</span><span class="sxs-lookup"><span data-stu-id="4875e-127">day</span></span>  <br/> |<span data-ttu-id="4875e-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="4875e-128">xs:string</span></span>  <br/> |<span data-ttu-id="4875e-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="4875e-129">optional</span></span>  <br/> |<span data-ttu-id="4875e-130">予測の 1 日を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="4875e-131">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="4875e-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4875e-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="4875e-132">feelslike</span></span>  <br/> |<span data-ttu-id="4875e-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4875e-133">xs:integer</span></span>  <br/> |<span data-ttu-id="4875e-134">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-134">required</span></span>  <br/> |<span data-ttu-id="4875e-135">ように現在の天気予報の気の温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="4875e-136">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="4875e-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4875e-137">湿度</span><span class="sxs-lookup"><span data-stu-id="4875e-137">humidity</span></span>  <br/> |<span data-ttu-id="4875e-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4875e-138">xs:integer</span></span>  <br/> |<span data-ttu-id="4875e-139">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-139">required</span></span>  <br/> |<span data-ttu-id="4875e-140">現在湿度の数値の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="4875e-141">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="4875e-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4875e-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="4875e-142">observationpoint</span></span>  <br/> |<span data-ttu-id="4875e-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="4875e-143">xs:string</span></span>  <br/> |<span data-ttu-id="4875e-144">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-144">required</span></span>  <br/> |<span data-ttu-id="4875e-145">現在の気象情報を確認する場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="4875e-146">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="4875e-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4875e-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="4875e-147">observationtime</span></span>  <br/> |<span data-ttu-id="4875e-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="4875e-148">xs:time</span></span>  <br/> |<span data-ttu-id="4875e-149">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-149">required</span></span>  <br/> |<span data-ttu-id="4875e-150">現在の気象情報を確認するときを指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="4875e-151">型 xs:time の値</span><span class="sxs-lookup"><span data-stu-id="4875e-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="4875e-152">shortday</span><span class="sxs-lookup"><span data-stu-id="4875e-152">shortday</span></span>  <br/> |<span data-ttu-id="4875e-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="4875e-153">xs:string</span></span>  <br/> |<span data-ttu-id="4875e-154">省略可能</span><span class="sxs-lookup"><span data-stu-id="4875e-154">optional</span></span>  <br/> |<span data-ttu-id="4875e-155">省略形で 1 日を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="4875e-156">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="4875e-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4875e-157">skycode</span><span class="sxs-lookup"><span data-stu-id="4875e-157">skycode</span></span>  <br/> |<span data-ttu-id="4875e-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4875e-158">xs:integer</span></span>  <br/> |<span data-ttu-id="4875e-159">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-159">required</span></span>  <br/> |<span data-ttu-id="4875e-160">現在の気象条件に整数コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="4875e-161">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="4875e-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4875e-162">skytext</span><span class="sxs-lookup"><span data-stu-id="4875e-162">skytext</span></span>  <br/> |<span data-ttu-id="4875e-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="4875e-163">xs:string</span></span>  <br/> |<span data-ttu-id="4875e-164">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-164">required</span></span>  <br/> |<span data-ttu-id="4875e-165">現在の気象条件を記述する 1、2 の単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="4875e-166">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="4875e-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4875e-167">温度</span><span class="sxs-lookup"><span data-stu-id="4875e-167">temperature</span></span>  <br/> |<span data-ttu-id="4875e-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4875e-168">xs:integer</span></span>  <br/> |<span data-ttu-id="4875e-169">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-169">required</span></span>  <br/> |<span data-ttu-id="4875e-170">場所の現在の温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="4875e-171">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="4875e-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="4875e-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="4875e-172">winddisplay</span></span>  <br/> |<span data-ttu-id="4875e-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="4875e-173">xs:string</span></span>  <br/> |<span data-ttu-id="4875e-174">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-174">required</span></span>  <br/> |<span data-ttu-id="4875e-175">現在の風の状況を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="4875e-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="4875e-176">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="4875e-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="4875e-177">風速</span><span class="sxs-lookup"><span data-stu-id="4875e-177">windspeed</span></span>  <br/> |<span data-ttu-id="4875e-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4875e-178">xs:integer</span></span>  <br/> |<span data-ttu-id="4875e-179">必須</span><span class="sxs-lookup"><span data-stu-id="4875e-179">required</span></span>  <br/> |<span data-ttu-id="4875e-180">現在の数値の風の速度の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="4875e-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="4875e-181">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="4875e-181">A value of the type xs:integer</span></span>  <br/> |
   

