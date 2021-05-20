---
title: forecastType complexType (Outlook天気予報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: 場所の天気予報天気予報に関するパラメーターを定義します。
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540953"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="47c10-103">forecastType complexType (Outlook天気予報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="47c10-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="47c10-104">場所の天気予報天気予報に関するパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="47c10-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="47c10-105">型情報</span><span class="sxs-lookup"><span data-stu-id="47c10-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47c10-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="47c10-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="47c10-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="47c10-107">**Schema file**</span></span> <br/> |<span data-ttu-id="47c10-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="47c10-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="47c10-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="47c10-109">**Extension base**</span></span> <br/> |<span data-ttu-id="47c10-110">なし</span><span class="sxs-lookup"><span data-stu-id="47c10-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="47c10-111">定義</span><span class="sxs-lookup"><span data-stu-id="47c10-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="47c10-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="47c10-112">Elements and attributes</span></span>

<span data-ttu-id="47c10-113">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="47c10-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="47c10-114">子要素</span><span class="sxs-lookup"><span data-stu-id="47c10-114">Child elements</span></span>

<span data-ttu-id="47c10-115">なし。</span><span class="sxs-lookup"><span data-stu-id="47c10-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47c10-116">属性</span><span class="sxs-lookup"><span data-stu-id="47c10-116">Attributes</span></span>

|<span data-ttu-id="47c10-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="47c10-117">**Attribute**</span></span>|<span data-ttu-id="47c10-118">**型**</span><span class="sxs-lookup"><span data-stu-id="47c10-118">**Type**</span></span>|<span data-ttu-id="47c10-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="47c10-119">**Required**</span></span>|<span data-ttu-id="47c10-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="47c10-120">**Description**</span></span>|<span data-ttu-id="47c10-121">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="47c10-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="47c10-122">date</span><span class="sxs-lookup"><span data-stu-id="47c10-122">date</span></span>  <br/> |<span data-ttu-id="47c10-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="47c10-123">xs:date</span></span>  <br/> |<span data-ttu-id="47c10-124">必須</span><span class="sxs-lookup"><span data-stu-id="47c10-124">required</span></span>  <br/> |<span data-ttu-id="47c10-125">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c10-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="47c10-126">xs:date 型の値</span><span class="sxs-lookup"><span data-stu-id="47c10-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="47c10-127">日</span><span class="sxs-lookup"><span data-stu-id="47c10-127">day</span></span>  <br/> |<span data-ttu-id="47c10-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="47c10-128">xs:string</span></span>  <br/> |<span data-ttu-id="47c10-129">必須</span><span class="sxs-lookup"><span data-stu-id="47c10-129">required</span></span>  <br/> |<span data-ttu-id="47c10-130">予測の日を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c10-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="47c10-131">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="47c10-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="47c10-132">high</span><span class="sxs-lookup"><span data-stu-id="47c10-132">high</span></span>  <br/> |<span data-ttu-id="47c10-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="47c10-133">xs:integer</span></span>  <br/> |<span data-ttu-id="47c10-134">必須</span><span class="sxs-lookup"><span data-stu-id="47c10-134">required</span></span>  <br/> |<span data-ttu-id="47c10-135">予測される最高温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c10-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="47c10-136">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="47c10-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="47c10-137">low</span><span class="sxs-lookup"><span data-stu-id="47c10-137">low</span></span>  <br/> |<span data-ttu-id="47c10-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="47c10-138">xs:integer</span></span>  <br/> |<span data-ttu-id="47c10-139">必須</span><span class="sxs-lookup"><span data-stu-id="47c10-139">required</span></span>  <br/> |<span data-ttu-id="47c10-140">予測される最低温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c10-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="47c10-141">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="47c10-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="47c10-142">precip</span><span class="sxs-lookup"><span data-stu-id="47c10-142">precip</span></span>  <br/> |<span data-ttu-id="47c10-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="47c10-143">xs:integer</span></span>  <br/> |<span data-ttu-id="47c10-144">必須</span><span class="sxs-lookup"><span data-stu-id="47c10-144">required</span></span>  <br/> |<span data-ttu-id="47c10-145">降水の可能性の割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c10-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="47c10-146">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="47c10-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="47c10-147">shortday</span><span class="sxs-lookup"><span data-stu-id="47c10-147">shortday</span></span>  <br/> |<span data-ttu-id="47c10-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="47c10-148">xs:string</span></span>  <br/> |<span data-ttu-id="47c10-149">必須</span><span class="sxs-lookup"><span data-stu-id="47c10-149">required</span></span>  <br/> |<span data-ttu-id="47c10-150">省略形で日を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c10-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="47c10-151">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="47c10-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="47c10-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="47c10-152">skycodeday</span></span>  <br/> |<span data-ttu-id="47c10-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="47c10-153">xs:integer</span></span>  <br/> |<span data-ttu-id="47c10-154">必須</span><span class="sxs-lookup"><span data-stu-id="47c10-154">required</span></span>  <br/> |<span data-ttu-id="47c10-155">予測条件のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="47c10-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="47c10-156">xs:integer 型の値</span><span class="sxs-lookup"><span data-stu-id="47c10-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="47c10-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="47c10-157">skytextday</span></span>  <br/> |<span data-ttu-id="47c10-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="47c10-158">xs:string</span></span>  <br/> |<span data-ttu-id="47c10-159">必須</span><span class="sxs-lookup"><span data-stu-id="47c10-159">required</span></span>  <br/> |<span data-ttu-id="47c10-160">予測条件を表す 1 から 2 つの単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c10-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="47c10-161">xs:string 型の値</span><span class="sxs-lookup"><span data-stu-id="47c10-161">A value of the type xs:string</span></span>  <br/> |
   

