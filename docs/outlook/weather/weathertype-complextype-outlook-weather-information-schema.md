---
title: weatherType complexType (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: 場所の天気予報の条件を指定します。
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355042"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="bda72-103">weatherType complexType (Outlook 天気情報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="bda72-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="bda72-104">場所の天気予報の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="bda72-105">型情報</span><span class="sxs-lookup"><span data-stu-id="bda72-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bda72-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bda72-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="bda72-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="bda72-107">**Schema file**</span></span> <br/> |<span data-ttu-id="bda72-108">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="bda72-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="bda72-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="bda72-109">**Extension base**</span></span> <br/> |<span data-ttu-id="bda72-110">なし</span><span class="sxs-lookup"><span data-stu-id="bda72-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bda72-111">定義</span><span class="sxs-lookup"><span data-stu-id="bda72-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bda72-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="bda72-112">Elements and attributes</span></span>

<span data-ttu-id="bda72-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bda72-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bda72-114">子要素</span><span class="sxs-lookup"><span data-stu-id="bda72-114">Child elements</span></span>

|<span data-ttu-id="bda72-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="bda72-115">**Element**</span></span>|<span data-ttu-id="bda72-116">**型**</span><span class="sxs-lookup"><span data-stu-id="bda72-116">**Type**</span></span>|<span data-ttu-id="bda72-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="bda72-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bda72-118">現在の</span><span class="sxs-lookup"><span data-stu-id="bda72-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="bda72-119">currenttype</span><span class="sxs-lookup"><span data-stu-id="bda72-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="bda72-120">現在の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="bda72-121">気象</span><span class="sxs-lookup"><span data-stu-id="bda72-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="bda72-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="bda72-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="bda72-123">今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。</span><span class="sxs-lookup"><span data-stu-id="bda72-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bda72-124">属性</span><span class="sxs-lookup"><span data-stu-id="bda72-124">Attributes</span></span>

|<span data-ttu-id="bda72-125">**属性**</span><span class="sxs-lookup"><span data-stu-id="bda72-125">**Attribute**</span></span>|<span data-ttu-id="bda72-126">**型**</span><span class="sxs-lookup"><span data-stu-id="bda72-126">**Type**</span></span>|<span data-ttu-id="bda72-127">**必須**</span><span class="sxs-lookup"><span data-stu-id="bda72-127">**Required**</span></span>|<span data-ttu-id="bda72-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="bda72-128">**Description**</span></span>|<span data-ttu-id="bda72-129">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="bda72-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bda72-130">帰属</span><span class="sxs-lookup"><span data-stu-id="bda72-130">attribution</span></span>  <br/> |<span data-ttu-id="bda72-131">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="bda72-131">xs:string</span></span>  <br/> |<span data-ttu-id="bda72-132">必須</span><span class="sxs-lookup"><span data-stu-id="bda72-132">required</span></span>  <br/> |<span data-ttu-id="bda72-133">天気情報のソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="bda72-134">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="bda72-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="bda72-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="bda72-135">degreetype</span></span>  <br/> |<span data-ttu-id="bda72-136">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="bda72-136">xs:string</span></span>  <br/> |<span data-ttu-id="bda72-137">必須</span><span class="sxs-lookup"><span data-stu-id="bda72-137">required</span></span>  <br/> |<span data-ttu-id="bda72-138">場所の温度の単位を指定します。たとえば、摂氏を指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="bda72-139">C、F</span><span class="sxs-lookup"><span data-stu-id="bda72-139">C, F</span></span>  <br/> |
|<span data-ttu-id="bda72-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="bda72-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="bda72-141">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="bda72-141">xs:string</span></span>  <br/> |<span data-ttu-id="bda72-142">必須</span><span class="sxs-lookup"><span data-stu-id="bda72-142">required</span></span>  <br/> |<span data-ttu-id="bda72-143">場所のイメージの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="bda72-144">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="bda72-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="bda72-145">timezone</span><span class="sxs-lookup"><span data-stu-id="bda72-145">timezone</span></span>  <br/> |<span data-ttu-id="bda72-146">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="bda72-146">xs:integer</span></span>  <br/> |<span data-ttu-id="bda72-147">必須</span><span class="sxs-lookup"><span data-stu-id="bda72-147">required</span></span>  <br/> |<span data-ttu-id="bda72-148">GMT オフセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="bda72-149">-11 から12の範囲の値</span><span class="sxs-lookup"><span data-stu-id="bda72-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="bda72-150">url</span><span class="sxs-lookup"><span data-stu-id="bda72-150">url</span></span>  <br/> |<span data-ttu-id="bda72-151">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="bda72-151">xs:string</span></span>  <br/> |<span data-ttu-id="bda72-152">必須</span><span class="sxs-lookup"><span data-stu-id="bda72-152">required</span></span>  <br/> |<span data-ttu-id="bda72-153">指定した場所の天気情報を含む天気予報サービスの web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="bda72-154">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="bda72-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="bda72-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="bda72-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="bda72-156">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="bda72-156">xs:string</span></span>  <br/> |<span data-ttu-id="bda72-157">必須</span><span class="sxs-lookup"><span data-stu-id="bda72-157">required</span></span>  <br/> |<span data-ttu-id="bda72-158">同じ名前を持つ複数の場所を区別するために使用される場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="bda72-159">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="bda72-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="bda72-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="bda72-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="bda72-161">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="bda72-161">xs:string</span></span>  <br/> |<span data-ttu-id="bda72-162">必須</span><span class="sxs-lookup"><span data-stu-id="bda72-162">required</span></span>  <br/> |<span data-ttu-id="bda72-163">ドロップダウンコントロールに表示される場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="bda72-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="bda72-164">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="bda72-164">A value of the type xs:string</span></span>  <br/> |
   

