---
title: weatherType complexType (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: 場所の気象条件を指定します。
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398767"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="6b67b-103">weatherType complexType (Outlook の気象情報のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="6b67b-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="6b67b-104">場所の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="6b67b-105">型情報</span><span class="sxs-lookup"><span data-stu-id="6b67b-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b67b-106">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="6b67b-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="6b67b-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="6b67b-107">**Schema file**</span></span> <br/> |<span data-ttu-id="6b67b-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="6b67b-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="6b67b-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="6b67b-109">**Extension base**</span></span> <br/> |<span data-ttu-id="6b67b-110">なし</span><span class="sxs-lookup"><span data-stu-id="6b67b-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b67b-111">定義</span><span class="sxs-lookup"><span data-stu-id="6b67b-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6b67b-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="6b67b-112">Elements and attributes</span></span>

<span data-ttu-id="6b67b-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b67b-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6b67b-114">子要素</span><span class="sxs-lookup"><span data-stu-id="6b67b-114">Child elements</span></span>

|<span data-ttu-id="6b67b-115">**要素**</span><span class="sxs-lookup"><span data-stu-id="6b67b-115">**Element**</span></span>|<span data-ttu-id="6b67b-116">**型**</span><span class="sxs-lookup"><span data-stu-id="6b67b-116">**Type**</span></span>|<span data-ttu-id="6b67b-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b67b-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b67b-118">現在の</span><span class="sxs-lookup"><span data-stu-id="6b67b-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="6b67b-119">currentType</span><span class="sxs-lookup"><span data-stu-id="6b67b-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="6b67b-120">現在の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="6b67b-121">予測</span><span class="sxs-lookup"><span data-stu-id="6b67b-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="6b67b-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="6b67b-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="6b67b-123">今日含めて後 3 日以上の今後の気象条件を指定する: 今日、明日、明後日。</span><span class="sxs-lookup"><span data-stu-id="6b67b-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6b67b-124">属性</span><span class="sxs-lookup"><span data-stu-id="6b67b-124">Attributes</span></span>

|<span data-ttu-id="6b67b-125">**属性**</span><span class="sxs-lookup"><span data-stu-id="6b67b-125">**Attribute**</span></span>|<span data-ttu-id="6b67b-126">**型**</span><span class="sxs-lookup"><span data-stu-id="6b67b-126">**Type**</span></span>|<span data-ttu-id="6b67b-127">**必須**</span><span class="sxs-lookup"><span data-stu-id="6b67b-127">**Required**</span></span>|<span data-ttu-id="6b67b-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b67b-128">**Description**</span></span>|<span data-ttu-id="6b67b-129">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="6b67b-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b67b-130">属性</span><span class="sxs-lookup"><span data-stu-id="6b67b-130">attribution</span></span>  <br/> |<span data-ttu-id="6b67b-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b67b-131">xs:string</span></span>  <br/> |<span data-ttu-id="6b67b-132">必須</span><span class="sxs-lookup"><span data-stu-id="6b67b-132">required</span></span>  <br/> |<span data-ttu-id="6b67b-133">気象情報のソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="6b67b-134">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="6b67b-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6b67b-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="6b67b-135">degreetype</span></span>  <br/> |<span data-ttu-id="6b67b-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b67b-136">xs:string</span></span>  <br/> |<span data-ttu-id="6b67b-137">必須</span><span class="sxs-lookup"><span data-stu-id="6b67b-137">required</span></span>  <br/> |<span data-ttu-id="6b67b-138">場所たとえば、摂氏の温度の単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="6b67b-139">C、F</span><span class="sxs-lookup"><span data-stu-id="6b67b-139">C, F</span></span>  <br/> |
|<span data-ttu-id="6b67b-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="6b67b-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="6b67b-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b67b-141">xs:string</span></span>  <br/> |<span data-ttu-id="6b67b-142">必須</span><span class="sxs-lookup"><span data-stu-id="6b67b-142">required</span></span>  <br/> |<span data-ttu-id="6b67b-143">場所のイメージの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="6b67b-144">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="6b67b-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6b67b-145">タイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="6b67b-145">timezone</span></span>  <br/> |<span data-ttu-id="6b67b-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6b67b-146">xs:integer</span></span>  <br/> |<span data-ttu-id="6b67b-147">必須</span><span class="sxs-lookup"><span data-stu-id="6b67b-147">required</span></span>  <br/> |<span data-ttu-id="6b67b-148">GMT オフセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="6b67b-149">-11 と 12 の間の値</span><span class="sxs-lookup"><span data-stu-id="6b67b-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="6b67b-150">url</span><span class="sxs-lookup"><span data-stu-id="6b67b-150">url</span></span>  <br/> |<span data-ttu-id="6b67b-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b67b-151">xs:string</span></span>  <br/> |<span data-ttu-id="6b67b-152">必須</span><span class="sxs-lookup"><span data-stu-id="6b67b-152">required</span></span>  <br/> |<span data-ttu-id="6b67b-153">指定した場所の気象情報を含む気象サービスの web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="6b67b-154">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="6b67b-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6b67b-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="6b67b-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="6b67b-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b67b-156">xs:string</span></span>  <br/> |<span data-ttu-id="6b67b-157">必須</span><span class="sxs-lookup"><span data-stu-id="6b67b-157">required</span></span>  <br/> |<span data-ttu-id="6b67b-158">同じ名前を持つ複数の場所を識別するために使用される場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="6b67b-159">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="6b67b-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6b67b-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="6b67b-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="6b67b-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="6b67b-161">xs:string</span></span>  <br/> |<span data-ttu-id="6b67b-162">必須</span><span class="sxs-lookup"><span data-stu-id="6b67b-162">required</span></span>  <br/> |<span data-ttu-id="6b67b-163">ドロップ ダウン コントロールに表示されている場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b67b-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="6b67b-164">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="6b67b-164">A value of the type xs:string</span></span>  <br/> |
   

