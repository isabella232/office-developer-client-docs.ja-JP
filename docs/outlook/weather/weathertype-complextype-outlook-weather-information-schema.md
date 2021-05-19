---
title: weatherType complexType (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: 場所の気象条件を指定します。
ms.openlocfilehash: ac7b8f37e71da203db0f6aefc8e20b29e810c3cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542948"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="eca36-103">weatherType complexType (Outlook天気予報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="eca36-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="eca36-104">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="eca36-105">型情報</span><span class="sxs-lookup"><span data-stu-id="eca36-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eca36-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eca36-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="eca36-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="eca36-107">**Schema file**</span></span> <br/> |<span data-ttu-id="eca36-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="eca36-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="eca36-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="eca36-109">**Extension base**</span></span> <br/> |<span data-ttu-id="eca36-110">なし</span><span class="sxs-lookup"><span data-stu-id="eca36-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eca36-111">定義</span><span class="sxs-lookup"><span data-stu-id="eca36-111">Definition</span></span>

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="eca36-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="eca36-112">Elements and attributes</span></span>

<span data-ttu-id="eca36-113">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="eca36-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eca36-114">子要素</span><span class="sxs-lookup"><span data-stu-id="eca36-114">Child elements</span></span>

|<span data-ttu-id="eca36-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="eca36-115">**Element**</span></span>|<span data-ttu-id="eca36-116">**型**</span><span class="sxs-lookup"><span data-stu-id="eca36-116">**Type**</span></span>|<span data-ttu-id="eca36-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="eca36-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eca36-118">現在の</span><span class="sxs-lookup"><span data-stu-id="eca36-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="eca36-119">currentType</span><span class="sxs-lookup"><span data-stu-id="eca36-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="eca36-120">現在の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="eca36-121">予測</span><span class="sxs-lookup"><span data-stu-id="eca36-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="eca36-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="eca36-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="eca36-123">今日、明日、明日の次の日を含む、少なくとも 3 日先の将来の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="eca36-124">属性</span><span class="sxs-lookup"><span data-stu-id="eca36-124">Attributes</span></span>

|<span data-ttu-id="eca36-125">**属性**</span><span class="sxs-lookup"><span data-stu-id="eca36-125">**Attribute**</span></span>|<span data-ttu-id="eca36-126">**型**</span><span class="sxs-lookup"><span data-stu-id="eca36-126">**Type**</span></span>|<span data-ttu-id="eca36-127">**必須**</span><span class="sxs-lookup"><span data-stu-id="eca36-127">**Required**</span></span>|<span data-ttu-id="eca36-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="eca36-128">**Description**</span></span>|<span data-ttu-id="eca36-129">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="eca36-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eca36-130">属性</span><span class="sxs-lookup"><span data-stu-id="eca36-130">attribution</span></span>  <br/> |<span data-ttu-id="eca36-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="eca36-131">xs:string</span></span>  <br/> |<span data-ttu-id="eca36-132">必須</span><span class="sxs-lookup"><span data-stu-id="eca36-132">required</span></span>  <br/> |<span data-ttu-id="eca36-133">天気予報情報のソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="eca36-134">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="eca36-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="eca36-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="eca36-135">degreetype</span></span>  <br/> |<span data-ttu-id="eca36-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="eca36-136">xs:string</span></span>  <br/> |<span data-ttu-id="eca36-137">必須</span><span class="sxs-lookup"><span data-stu-id="eca36-137">required</span></span>  <br/> |<span data-ttu-id="eca36-138">場所の温度 (摂氏など) の単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="eca36-139">C、F</span><span class="sxs-lookup"><span data-stu-id="eca36-139">C, F</span></span>  <br/> |
|<span data-ttu-id="eca36-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="eca36-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="eca36-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="eca36-141">xs:string</span></span>  <br/> |<span data-ttu-id="eca36-142">必須</span><span class="sxs-lookup"><span data-stu-id="eca36-142">required</span></span>  <br/> |<span data-ttu-id="eca36-143">場所のイメージの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="eca36-144">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="eca36-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="eca36-145">timezone</span><span class="sxs-lookup"><span data-stu-id="eca36-145">timezone</span></span>  <br/> |<span data-ttu-id="eca36-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="eca36-146">xs:integer</span></span>  <br/> |<span data-ttu-id="eca36-147">必須</span><span class="sxs-lookup"><span data-stu-id="eca36-147">required</span></span>  <br/> |<span data-ttu-id="eca36-148">GMT オフセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="eca36-149">-11 ~ 12 の値</span><span class="sxs-lookup"><span data-stu-id="eca36-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="eca36-150">url</span><span class="sxs-lookup"><span data-stu-id="eca36-150">url</span></span>  <br/> |<span data-ttu-id="eca36-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="eca36-151">xs:string</span></span>  <br/> |<span data-ttu-id="eca36-152">必須</span><span class="sxs-lookup"><span data-stu-id="eca36-152">required</span></span>  <br/> |<span data-ttu-id="eca36-153">指定した場所の天気予報情報を含む天気予報サービスの Web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="eca36-154">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="eca36-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="eca36-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="eca36-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="eca36-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="eca36-156">xs:string</span></span>  <br/> |<span data-ttu-id="eca36-157">必須</span><span class="sxs-lookup"><span data-stu-id="eca36-157">required</span></span>  <br/> |<span data-ttu-id="eca36-158">同じ名前を持つ複数の場所を区別するために使用する場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="eca36-159">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="eca36-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="eca36-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="eca36-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="eca36-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="eca36-161">xs:string</span></span>  <br/> |<span data-ttu-id="eca36-162">必須</span><span class="sxs-lookup"><span data-stu-id="eca36-162">required</span></span>  <br/> |<span data-ttu-id="eca36-163">ドロップダウン コントロールに表示される場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="eca36-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="eca36-164">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="eca36-164">A value of the type xs:string</span></span>  <br/> |
   

