---
title: forecastType complexType (Outlook の気象情報のスキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: 場所の予測の気象条件のパラメーターを定義します。
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804468"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="a9d60-103">forecastType complexType (Outlook の気象情報のスキーマ)</span><span class="sxs-lookup"><span data-stu-id="a9d60-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="a9d60-104">場所の予測の気象条件のパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="a9d60-105">型情報</span><span class="sxs-lookup"><span data-stu-id="a9d60-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9d60-106">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a9d60-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="a9d60-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a9d60-107">**Schema file**</span></span> <br/> |<span data-ttu-id="a9d60-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="a9d60-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="a9d60-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="a9d60-109">**Extension base**</span></span> <br/> |<span data-ttu-id="a9d60-110">なし</span><span class="sxs-lookup"><span data-stu-id="a9d60-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a9d60-111">定義</span><span class="sxs-lookup"><span data-stu-id="a9d60-111">Definition</span></span>

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="a9d60-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a9d60-112">Elements and attributes</span></span>

<span data-ttu-id="a9d60-113">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9d60-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a9d60-114">子要素</span><span class="sxs-lookup"><span data-stu-id="a9d60-114">Child elements</span></span>

<span data-ttu-id="a9d60-115">なし。</span><span class="sxs-lookup"><span data-stu-id="a9d60-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9d60-116">属性</span><span class="sxs-lookup"><span data-stu-id="a9d60-116">Attributes</span></span>

|<span data-ttu-id="a9d60-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="a9d60-117">**Attribute**</span></span>|<span data-ttu-id="a9d60-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a9d60-118">**Type**</span></span>|<span data-ttu-id="a9d60-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="a9d60-119">**Required**</span></span>|<span data-ttu-id="a9d60-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="a9d60-120">**Description**</span></span>|<span data-ttu-id="a9d60-121">**使用可能な値**</span><span class="sxs-lookup"><span data-stu-id="a9d60-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a9d60-122">date</span><span class="sxs-lookup"><span data-stu-id="a9d60-122">date</span></span>  <br/> |<span data-ttu-id="a9d60-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="a9d60-123">xs:date</span></span>  <br/> |<span data-ttu-id="a9d60-124">必須</span><span class="sxs-lookup"><span data-stu-id="a9d60-124">required</span></span>  <br/> |<span data-ttu-id="a9d60-125">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="a9d60-126">型 xs:date の値</span><span class="sxs-lookup"><span data-stu-id="a9d60-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="a9d60-127">1 日</span><span class="sxs-lookup"><span data-stu-id="a9d60-127">day</span></span>  <br/> |<span data-ttu-id="a9d60-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="a9d60-128">xs:string</span></span>  <br/> |<span data-ttu-id="a9d60-129">必須</span><span class="sxs-lookup"><span data-stu-id="a9d60-129">required</span></span>  <br/> |<span data-ttu-id="a9d60-130">予測の 1 日を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="a9d60-131">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="a9d60-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a9d60-132">高</span><span class="sxs-lookup"><span data-stu-id="a9d60-132">high</span></span>  <br/> |<span data-ttu-id="a9d60-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a9d60-133">xs:integer</span></span>  <br/> |<span data-ttu-id="a9d60-134">必須</span><span class="sxs-lookup"><span data-stu-id="a9d60-134">required</span></span>  <br/> |<span data-ttu-id="a9d60-135">予測の最高温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="a9d60-136">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="a9d60-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="a9d60-137">低</span><span class="sxs-lookup"><span data-stu-id="a9d60-137">low</span></span>  <br/> |<span data-ttu-id="a9d60-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a9d60-138">xs:integer</span></span>  <br/> |<span data-ttu-id="a9d60-139">必須</span><span class="sxs-lookup"><span data-stu-id="a9d60-139">required</span></span>  <br/> |<span data-ttu-id="a9d60-140">予測の最低温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="a9d60-141">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="a9d60-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="a9d60-142">precip</span><span class="sxs-lookup"><span data-stu-id="a9d60-142">precip</span></span>  <br/> |<span data-ttu-id="a9d60-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a9d60-143">xs:integer</span></span>  <br/> |<span data-ttu-id="a9d60-144">必須</span><span class="sxs-lookup"><span data-stu-id="a9d60-144">required</span></span>  <br/> |<span data-ttu-id="a9d60-145">降水の発生する可能性の割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="a9d60-146">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="a9d60-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="a9d60-147">shortday</span><span class="sxs-lookup"><span data-stu-id="a9d60-147">shortday</span></span>  <br/> |<span data-ttu-id="a9d60-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="a9d60-148">xs:string</span></span>  <br/> |<span data-ttu-id="a9d60-149">必須</span><span class="sxs-lookup"><span data-stu-id="a9d60-149">required</span></span>  <br/> |<span data-ttu-id="a9d60-150">省略形で 1 日を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="a9d60-151">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="a9d60-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a9d60-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="a9d60-152">skycodeday</span></span>  <br/> |<span data-ttu-id="a9d60-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a9d60-153">xs:integer</span></span>  <br/> |<span data-ttu-id="a9d60-154">必須</span><span class="sxs-lookup"><span data-stu-id="a9d60-154">required</span></span>  <br/> |<span data-ttu-id="a9d60-155">予測の条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="a9d60-156">型 xs:integer の値</span><span class="sxs-lookup"><span data-stu-id="a9d60-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="a9d60-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="a9d60-157">skytextday</span></span>  <br/> |<span data-ttu-id="a9d60-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="a9d60-158">xs:string</span></span>  <br/> |<span data-ttu-id="a9d60-159">必須</span><span class="sxs-lookup"><span data-stu-id="a9d60-159">required</span></span>  <br/> |<span data-ttu-id="a9d60-160">予測の条件を説明する 1、2 語を指定します。</span><span class="sxs-lookup"><span data-stu-id="a9d60-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="a9d60-161">値の型の使用されています</span><span class="sxs-lookup"><span data-stu-id="a9d60-161">A value of the type xs:string</span></span>  <br/> |
   

