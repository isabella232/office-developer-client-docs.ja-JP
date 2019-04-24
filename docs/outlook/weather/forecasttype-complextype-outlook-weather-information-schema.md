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
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361146"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="2e0c7-103">forecastType complexType (Outlook 天気情報スキーマ)</span><span class="sxs-lookup"><span data-stu-id="2e0c7-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="2e0c7-104">場所の天気予報の条件に関するパラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="2e0c7-105">型情報</span><span class="sxs-lookup"><span data-stu-id="2e0c7-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e0c7-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2e0c7-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="2e0c7-107">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="2e0c7-107">**Schema file**</span></span> <br/> |<span data-ttu-id="2e0c7-108">getweatherinfo</span><span class="sxs-lookup"><span data-stu-id="2e0c7-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="2e0c7-109">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="2e0c7-109">**Extension base**</span></span> <br/> |<span data-ttu-id="2e0c7-110">なし</span><span class="sxs-lookup"><span data-stu-id="2e0c7-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2e0c7-111">定義</span><span class="sxs-lookup"><span data-stu-id="2e0c7-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2e0c7-112">要素と属性</span><span class="sxs-lookup"><span data-stu-id="2e0c7-112">Elements and attributes</span></span>

<span data-ttu-id="2e0c7-113">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2e0c7-114">子要素</span><span class="sxs-lookup"><span data-stu-id="2e0c7-114">Child elements</span></span>

<span data-ttu-id="2e0c7-115">なし。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e0c7-116">属性</span><span class="sxs-lookup"><span data-stu-id="2e0c7-116">Attributes</span></span>

|<span data-ttu-id="2e0c7-117">**属性**</span><span class="sxs-lookup"><span data-stu-id="2e0c7-117">**Attribute**</span></span>|<span data-ttu-id="2e0c7-118">**型**</span><span class="sxs-lookup"><span data-stu-id="2e0c7-118">**Type**</span></span>|<span data-ttu-id="2e0c7-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="2e0c7-119">**Required**</span></span>|<span data-ttu-id="2e0c7-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="2e0c7-120">**Description**</span></span>|<span data-ttu-id="2e0c7-121">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="2e0c7-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2e0c7-122">日付</span><span class="sxs-lookup"><span data-stu-id="2e0c7-122">date</span></span>  <br/> |<span data-ttu-id="2e0c7-123">xs: date</span><span class="sxs-lookup"><span data-stu-id="2e0c7-123">xs:date</span></span>  <br/> |<span data-ttu-id="2e0c7-124">必須</span><span class="sxs-lookup"><span data-stu-id="2e0c7-124">required</span></span>  <br/> |<span data-ttu-id="2e0c7-125">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="2e0c7-126">xs: date 型の値</span><span class="sxs-lookup"><span data-stu-id="2e0c7-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="2e0c7-127">日勤</span><span class="sxs-lookup"><span data-stu-id="2e0c7-127">day</span></span>  <br/> |<span data-ttu-id="2e0c7-128">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="2e0c7-128">xs:string</span></span>  <br/> |<span data-ttu-id="2e0c7-129">必須</span><span class="sxs-lookup"><span data-stu-id="2e0c7-129">required</span></span>  <br/> |<span data-ttu-id="2e0c7-130">予測の日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="2e0c7-131">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="2e0c7-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2e0c7-132">高額</span><span class="sxs-lookup"><span data-stu-id="2e0c7-132">high</span></span>  <br/> |<span data-ttu-id="2e0c7-133">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="2e0c7-133">xs:integer</span></span>  <br/> |<span data-ttu-id="2e0c7-134">必須</span><span class="sxs-lookup"><span data-stu-id="2e0c7-134">required</span></span>  <br/> |<span data-ttu-id="2e0c7-135">予測最高温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="2e0c7-136">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="2e0c7-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2e0c7-137">低さ</span><span class="sxs-lookup"><span data-stu-id="2e0c7-137">low</span></span>  <br/> |<span data-ttu-id="2e0c7-138">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="2e0c7-138">xs:integer</span></span>  <br/> |<span data-ttu-id="2e0c7-139">必須</span><span class="sxs-lookup"><span data-stu-id="2e0c7-139">required</span></span>  <br/> |<span data-ttu-id="2e0c7-140">予測される最低温度を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="2e0c7-141">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="2e0c7-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2e0c7-142">precip</span><span class="sxs-lookup"><span data-stu-id="2e0c7-142">precip</span></span>  <br/> |<span data-ttu-id="2e0c7-143">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="2e0c7-143">xs:integer</span></span>  <br/> |<span data-ttu-id="2e0c7-144">必須</span><span class="sxs-lookup"><span data-stu-id="2e0c7-144">required</span></span>  <br/> |<span data-ttu-id="2e0c7-145">降水のパーセンテージを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="2e0c7-146">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="2e0c7-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2e0c7-147">短い日</span><span class="sxs-lookup"><span data-stu-id="2e0c7-147">shortday</span></span>  <br/> |<span data-ttu-id="2e0c7-148">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="2e0c7-148">xs:string</span></span>  <br/> |<span data-ttu-id="2e0c7-149">必須</span><span class="sxs-lookup"><span data-stu-id="2e0c7-149">required</span></span>  <br/> |<span data-ttu-id="2e0c7-150">日付を省略された形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="2e0c7-151">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="2e0c7-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2e0c7-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="2e0c7-152">skycodeday</span></span>  <br/> |<span data-ttu-id="2e0c7-153">xs: 整数</span><span class="sxs-lookup"><span data-stu-id="2e0c7-153">xs:integer</span></span>  <br/> |<span data-ttu-id="2e0c7-154">必須</span><span class="sxs-lookup"><span data-stu-id="2e0c7-154">required</span></span>  <br/> |<span data-ttu-id="2e0c7-155">予測される条件のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="2e0c7-156">xs: integer 型の値</span><span class="sxs-lookup"><span data-stu-id="2e0c7-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="2e0c7-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="2e0c7-157">skytextday</span></span>  <br/> |<span data-ttu-id="2e0c7-158">xs: 文字列</span><span class="sxs-lookup"><span data-stu-id="2e0c7-158">xs:string</span></span>  <br/> |<span data-ttu-id="2e0c7-159">必須</span><span class="sxs-lookup"><span data-stu-id="2e0c7-159">required</span></span>  <br/> |<span data-ttu-id="2e0c7-160">予測条件を説明する 1 ~ 2 単語を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e0c7-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="2e0c7-161">xs: 文字列型の値</span><span class="sxs-lookup"><span data-stu-id="2e0c7-161">A value of the type xs:string</span></span>  <br/> |
   

