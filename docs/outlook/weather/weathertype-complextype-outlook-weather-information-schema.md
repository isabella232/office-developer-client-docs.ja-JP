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
ms.openlocfilehash: ac7b8f37e71da203db0f6aefc8e20b29e810c3cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542948"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="a935e-103">weatherType complexType (Outlook 天気情報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="a935e-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="a935e-104">場所の天気予報の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="a935e-105">型情報</span><span class="sxs-lookup"><span data-stu-id="a935e-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a935e-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a935e-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="a935e-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a935e-107">**Schema file**</span></span> <br/> |<span data-ttu-id="a935e-108">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="a935e-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="a935e-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a935e-109">**Extension base**</span></span> <br/> |<span data-ttu-id="a935e-110">None</span><span class="sxs-lookup"><span data-stu-id="a935e-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a935e-111">定義</span><span class="sxs-lookup"><span data-stu-id="a935e-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a935e-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a935e-112">Elements and attributes</span></span>

<span data-ttu-id="a935e-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a935e-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a935e-114">子要素</span><span class="sxs-lookup"><span data-stu-id="a935e-114">Child elements</span></span>

|<span data-ttu-id="a935e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a935e-115">**Element**</span></span>|<span data-ttu-id="a935e-116">**型**</span><span class="sxs-lookup"><span data-stu-id="a935e-116">**Type**</span></span>|<span data-ttu-id="a935e-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="a935e-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a935e-118">現在の</span><span class="sxs-lookup"><span data-stu-id="a935e-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="a935e-119">currentType</span><span class="sxs-lookup"><span data-stu-id="a935e-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="a935e-120">現在の気象条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="a935e-121">気象</span><span class="sxs-lookup"><span data-stu-id="a935e-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="a935e-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="a935e-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="a935e-123">今日を含む少なくとも3日間の将来の気象条件を指定します。今日、明日、翌日以降。</span><span class="sxs-lookup"><span data-stu-id="a935e-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a935e-124">属性</span><span class="sxs-lookup"><span data-stu-id="a935e-124">Attributes</span></span>

|<span data-ttu-id="a935e-125">**属性**</span><span class="sxs-lookup"><span data-stu-id="a935e-125">**Attribute**</span></span>|<span data-ttu-id="a935e-126">**型**</span><span class="sxs-lookup"><span data-stu-id="a935e-126">**Type**</span></span>|<span data-ttu-id="a935e-127">**必須**</span><span class="sxs-lookup"><span data-stu-id="a935e-127">**Required**</span></span>|<span data-ttu-id="a935e-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="a935e-128">**Description**</span></span>|<span data-ttu-id="a935e-129">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="a935e-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a935e-130">帰属</span><span class="sxs-lookup"><span data-stu-id="a935e-130">attribution</span></span>  <br/> |<span data-ttu-id="a935e-131">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="a935e-131">xs:string</span></span>  <br/> |<span data-ttu-id="a935e-132">必須</span><span class="sxs-lookup"><span data-stu-id="a935e-132">required</span></span>  <br/> |<span data-ttu-id="a935e-133">天気情報のソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="a935e-134">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="a935e-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a935e-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="a935e-135">degreetype</span></span>  <br/> |<span data-ttu-id="a935e-136">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="a935e-136">xs:string</span></span>  <br/> |<span data-ttu-id="a935e-137">必須</span><span class="sxs-lookup"><span data-stu-id="a935e-137">required</span></span>  <br/> |<span data-ttu-id="a935e-138">場所の温度の単位を指定します。たとえば、摂氏を指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="a935e-139">C、F</span><span class="sxs-lookup"><span data-stu-id="a935e-139">C, F</span></span>  <br/> |
|<span data-ttu-id="a935e-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="a935e-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="a935e-141">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="a935e-141">xs:string</span></span>  <br/> |<span data-ttu-id="a935e-142">必須</span><span class="sxs-lookup"><span data-stu-id="a935e-142">required</span></span>  <br/> |<span data-ttu-id="a935e-143">場所のイメージの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="a935e-144">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="a935e-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a935e-145">timezone</span><span class="sxs-lookup"><span data-stu-id="a935e-145">timezone</span></span>  <br/> |<span data-ttu-id="a935e-146">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="a935e-146">xs:integer</span></span>  <br/> |<span data-ttu-id="a935e-147">必須</span><span class="sxs-lookup"><span data-stu-id="a935e-147">required</span></span>  <br/> |<span data-ttu-id="a935e-148">GMT オフセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="a935e-149">-11 から12の範囲の値</span><span class="sxs-lookup"><span data-stu-id="a935e-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="a935e-150">url</span><span class="sxs-lookup"><span data-stu-id="a935e-150">url</span></span>  <br/> |<span data-ttu-id="a935e-151">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="a935e-151">xs:string</span></span>  <br/> |<span data-ttu-id="a935e-152">必須</span><span class="sxs-lookup"><span data-stu-id="a935e-152">required</span></span>  <br/> |<span data-ttu-id="a935e-153">指定した場所の天気情報を含む天気予報サービスの web ページの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="a935e-154">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="a935e-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a935e-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="a935e-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="a935e-156">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="a935e-156">xs:string</span></span>  <br/> |<span data-ttu-id="a935e-157">必須</span><span class="sxs-lookup"><span data-stu-id="a935e-157">required</span></span>  <br/> |<span data-ttu-id="a935e-158">同じ名前を持つ複数の場所を区別するために使用される場所に関連付けられているコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="a935e-159">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="a935e-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a935e-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="a935e-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="a935e-161">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="a935e-161">xs:string</span></span>  <br/> |<span data-ttu-id="a935e-162">必須</span><span class="sxs-lookup"><span data-stu-id="a935e-162">required</span></span>  <br/> |<span data-ttu-id="a935e-163">ドロップダウンコントロールに表示される場所の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="a935e-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="a935e-164">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="a935e-164">A value of the type xs:string</span></span>  <br/> |
   

