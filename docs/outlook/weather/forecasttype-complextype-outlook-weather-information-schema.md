---
title: forecastType complexType (Outlook 天気情報スキーマ)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: 場所の天気予報の条件に関するパラメーターを定義します。
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540953"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="2999b-103">forecastType complexType (Outlook 天気情報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="2999b-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="2999b-104">場所の天気予報の条件に関するパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="2999b-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="2999b-105">型情報</span><span class="sxs-lookup"><span data-stu-id="2999b-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2999b-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2999b-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="2999b-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2999b-107">**Schema file**</span></span> <br/> |<span data-ttu-id="2999b-108">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="2999b-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="2999b-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="2999b-109">**Extension base**</span></span> <br/> |<span data-ttu-id="2999b-110">None</span><span class="sxs-lookup"><span data-stu-id="2999b-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2999b-111">定義</span><span class="sxs-lookup"><span data-stu-id="2999b-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2999b-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2999b-112">Elements and attributes</span></span>

<span data-ttu-id="2999b-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2999b-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2999b-114">子要素</span><span class="sxs-lookup"><span data-stu-id="2999b-114">Child elements</span></span>

<span data-ttu-id="2999b-115">なし。</span><span class="sxs-lookup"><span data-stu-id="2999b-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2999b-116">属性</span><span class="sxs-lookup"><span data-stu-id="2999b-116">Attributes</span></span>

|<span data-ttu-id="2999b-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="2999b-117">**Attribute**</span></span>|<span data-ttu-id="2999b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="2999b-118">**Type**</span></span>|<span data-ttu-id="2999b-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="2999b-119">**Required**</span></span>|<span data-ttu-id="2999b-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="2999b-120">**Description**</span></span>|<span data-ttu-id="2999b-121">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="2999b-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2999b-122">date</span><span class="sxs-lookup"><span data-stu-id="2999b-122">date</span></span>  <br/> |<span data-ttu-id="2999b-123">xs: date</span><span class="sxs-lookup"><span data-stu-id="2999b-123">xs:date</span></span>  <br/> |<span data-ttu-id="2999b-124">必須</span><span class="sxs-lookup"><span data-stu-id="2999b-124">required</span></span>  <br/> |<span data-ttu-id="2999b-125">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="2999b-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="2999b-126">Xs: date 型の値</span><span class="sxs-lookup"><span data-stu-id="2999b-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="2999b-127">日勤</span><span class="sxs-lookup"><span data-stu-id="2999b-127">day</span></span>  <br/> |<span data-ttu-id="2999b-128">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="2999b-128">xs:string</span></span>  <br/> |<span data-ttu-id="2999b-129">必須</span><span class="sxs-lookup"><span data-stu-id="2999b-129">required</span></span>  <br/> |<span data-ttu-id="2999b-130">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="2999b-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="2999b-131">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="2999b-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2999b-132">高額</span><span class="sxs-lookup"><span data-stu-id="2999b-132">high</span></span>  <br/> |<span data-ttu-id="2999b-133">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="2999b-133">xs:integer</span></span>  <br/> |<span data-ttu-id="2999b-134">必須</span><span class="sxs-lookup"><span data-stu-id="2999b-134">required</span></span>  <br/> |<span data-ttu-id="2999b-135">予測最高温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="2999b-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="2999b-136">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="2999b-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2999b-137">低さ</span><span class="sxs-lookup"><span data-stu-id="2999b-137">low</span></span>  <br/> |<span data-ttu-id="2999b-138">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="2999b-138">xs:integer</span></span>  <br/> |<span data-ttu-id="2999b-139">必須</span><span class="sxs-lookup"><span data-stu-id="2999b-139">required</span></span>  <br/> |<span data-ttu-id="2999b-140">予測される最低温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="2999b-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="2999b-141">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="2999b-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2999b-142">precip</span><span class="sxs-lookup"><span data-stu-id="2999b-142">precip</span></span>  <br/> |<span data-ttu-id="2999b-143">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="2999b-143">xs:integer</span></span>  <br/> |<span data-ttu-id="2999b-144">必須</span><span class="sxs-lookup"><span data-stu-id="2999b-144">required</span></span>  <br/> |<span data-ttu-id="2999b-145">降水のパーセンテージを指定します。</span><span class="sxs-lookup"><span data-stu-id="2999b-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="2999b-146">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="2999b-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2999b-147">短い日</span><span class="sxs-lookup"><span data-stu-id="2999b-147">shortday</span></span>  <br/> |<span data-ttu-id="2999b-148">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="2999b-148">xs:string</span></span>  <br/> |<span data-ttu-id="2999b-149">必須</span><span class="sxs-lookup"><span data-stu-id="2999b-149">required</span></span>  <br/> |<span data-ttu-id="2999b-150">日付を省略された形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="2999b-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="2999b-151">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="2999b-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2999b-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="2999b-152">skycodeday</span></span>  <br/> |<span data-ttu-id="2999b-153">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="2999b-153">xs:integer</span></span>  <br/> |<span data-ttu-id="2999b-154">必須</span><span class="sxs-lookup"><span data-stu-id="2999b-154">required</span></span>  <br/> |<span data-ttu-id="2999b-155">予測される条件のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="2999b-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="2999b-156">Xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="2999b-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2999b-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="2999b-157">skytextday</span></span>  <br/> |<span data-ttu-id="2999b-158">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="2999b-158">xs:string</span></span>  <br/> |<span data-ttu-id="2999b-159">必須</span><span class="sxs-lookup"><span data-stu-id="2999b-159">required</span></span>  <br/> |<span data-ttu-id="2999b-160">予測条件を説明する 1 ~ 2 単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="2999b-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="2999b-161">Xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="2999b-161">A value of the type xs:string</span></span>  <br/> |
   

