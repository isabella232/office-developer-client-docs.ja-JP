---
title: プロパティ識別子の範囲
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328533"
---
# <a name="property-identifier-ranges"></a><span data-ttu-id="a410a-103">プロパティ識別子の範囲</span><span class="sxs-lookup"><span data-stu-id="a410a-103">Property Identifier Ranges</span></span>

  
  
<span data-ttu-id="a410a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a410a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a410a-105">次の表は、各範囲のプロパティの所有者を説明する、プロパティ識別子のさまざまな範囲を要約したものです。</span><span class="sxs-lookup"><span data-stu-id="a410a-105">The following table summarizes the different ranges for property identifiers, describing the owner for the properties in each range.</span></span>
  
|<span data-ttu-id="a410a-106">**識別子の範囲**</span><span class="sxs-lookup"><span data-stu-id="a410a-106">**Identifier range**</span></span>|<span data-ttu-id="a410a-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="a410a-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a410a-108">0000</span><span class="sxs-lookup"><span data-stu-id="a410a-108">0000</span></span>  <br/> |<span data-ttu-id="a410a-109">特別な値**PR_NULL**のために MAPI によって予約されています。</span><span class="sxs-lookup"><span data-stu-id="a410a-109">Reserved by MAPI for the special value **PR_NULL**.</span></span>  <br/> |
|<span data-ttu-id="a410a-110">0001-0bff</span><span class="sxs-lookup"><span data-stu-id="a410a-110">0001 - 0BFF</span></span>  <br/> |<span data-ttu-id="a410a-111">メッセージエンベローププロパティ (MAPI によって定義されます)。</span><span class="sxs-lookup"><span data-stu-id="a410a-111">Message envelope properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="a410a-112">0c00-右から右</span><span class="sxs-lookup"><span data-stu-id="a410a-112">0C00 - 0DFF</span></span>  <br/> |<span data-ttu-id="a410a-113">MAPI によって定義された受信者のプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-113">Recipient properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="a410a-114">0e00-0fff</span><span class="sxs-lookup"><span data-stu-id="a410a-114">0E00 - 0FFF</span></span>  <br/> |<span data-ttu-id="a410a-115">MAPI で定義されている、非表示のテーブルメッセージプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-115">Non-transmittable message properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="a410a-116">1000-2fff</span><span class="sxs-lookup"><span data-stu-id="a410a-116">1000 - 2FFF</span></span>  <br/> |<span data-ttu-id="a410a-117">MAPI によって定義されたメッセージコンテンツのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-117">Message content properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="a410a-118">3000-3fff</span><span class="sxs-lookup"><span data-stu-id="a410a-118">3000 - 3FFF</span></span>  <br/> |<span data-ttu-id="a410a-119">MAPI によって定義されたメッセージと受信者以外のオブジェクトのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-119">Properties for objects other than messages and recipients defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="a410a-120">4000-57ff</span><span class="sxs-lookup"><span data-stu-id="a410a-120">4000 - 57FF</span></span>  <br/> |<span data-ttu-id="a410a-121">トランスポートプロバイダーによって定義されたメッセージエンベローププロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-121">Message envelope properties defined by transport providers.</span></span>  <br/> |
|<span data-ttu-id="a410a-122">5800-5fff</span><span class="sxs-lookup"><span data-stu-id="a410a-122">5800 - 5FFF</span></span>  <br/> |<span data-ttu-id="a410a-123">トランスポートプロバイダーとアドレス帳プロバイダーによって定義された受信者プロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-123">Recipient properties defined by transport and address book providers.</span></span>  <br/> |
|<span data-ttu-id="a410a-124">6000-65ff</span><span class="sxs-lookup"><span data-stu-id="a410a-124">6000 - 65FF</span></span>  <br/> |<span data-ttu-id="a410a-125">クライアントによって定義された、非表示のテーブルメッセージプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-125">Non-transmittable message properties defined by clients.</span></span>  <br/> |
|<span data-ttu-id="a410a-126">6600-67ff</span><span class="sxs-lookup"><span data-stu-id="a410a-126">6600 - 67FF</span></span>  <br/> |<span data-ttu-id="a410a-127">サービスプロバイダによって定義された、非アウトなテーブルプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-127">Non-transmittable properties defined by a service provider.</span></span> <span data-ttu-id="a410a-128">これらのプロパティは、ユーザーに対して表示または非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a410a-128">These properties can be visible or invisible to users.</span></span>  <br/> |
|<span data-ttu-id="a410a-129">6800 ~ 7BFF</span><span class="sxs-lookup"><span data-stu-id="a410a-129">6800 - 7BFF</span></span>  <br/> |<span data-ttu-id="a410a-130">これらのクラスの作成者によって定義されたカスタムメッセージクラスのメッセージコンテンツプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-130">Message content properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="a410a-131">7C00-7fff</span><span class="sxs-lookup"><span data-stu-id="a410a-131">7C00 - 7FFF</span></span>  <br/> |<span data-ttu-id="a410a-132">これらのクラスの作成者によって定義されたカスタムメッセージクラスの、非パススルーテーブルプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-132">Non-transmittable properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="a410a-133">8000 ~ FFFE</span><span class="sxs-lookup"><span data-stu-id="a410a-133">8000 - FFFE</span></span>  <br/> |<span data-ttu-id="a410a-134">クライアントと、場合によっては[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)および[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを使用して名前で識別される、サービスプロバイダーによって定義されるプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-134">Properties defined by clients and occasionally service providers that are identified by name through the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span>  <br/> |
|<span data-ttu-id="a410a-135">FFFF</span><span class="sxs-lookup"><span data-stu-id="a410a-135">FFFF</span></span>  <br/> |<span data-ttu-id="a410a-136">特別なエラー値 PROP_ID_INVALID に対して MAPI によって予約されています。</span><span class="sxs-lookup"><span data-stu-id="a410a-136">Reserved by MAPI for the special error value PROP_ID_INVALID.</span></span>  <br/> |
   
<span data-ttu-id="a410a-137">3000と3fff の範囲は、メッセージまたは受信者に関連付けられていないプロパティに対して予約されています。</span><span class="sxs-lookup"><span data-stu-id="a410a-137">The range between 3000 and 3FFF is reserved for properties that are not related to either messages or recipients.</span></span> <span data-ttu-id="a410a-138">MAPI は、オブジェクトの種類によって、この範囲をサブ範囲に分割します。次の表に、この詳細な内訳を示します。</span><span class="sxs-lookup"><span data-stu-id="a410a-138">MAPI divides this range into sub-ranges by types of object; the following table shows this further breakdown.</span></span> 
  
|<span data-ttu-id="a410a-139">**識別子の範囲**</span><span class="sxs-lookup"><span data-stu-id="a410a-139">**Identifier range**</span></span>|<span data-ttu-id="a410a-140">**プロパティの種類**</span><span class="sxs-lookup"><span data-stu-id="a410a-140">**Type of property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a410a-141">3000 ~ 33 ff</span><span class="sxs-lookup"><span data-stu-id="a410a-141">3000 - 33FF</span></span>  <br/> |<span data-ttu-id="a410a-142">**PR_DISPLAY_NAME**や**PR_ENTRYID**などの複数のオブジェクトに表示される共通のプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a410a-142">Common properties that appear on multiple objects, such as **PR_DISPLAY_NAME** and **PR_ENTRYID**.</span></span>  <br/> |
|<span data-ttu-id="a410a-143">3400-35ff</span><span class="sxs-lookup"><span data-stu-id="a410a-143">3400 - 35FF</span></span>  <br/> |<span data-ttu-id="a410a-144">メッセージストアのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a410a-144">Message store properties</span></span>  <br/> |
|<span data-ttu-id="a410a-145">3600-36ff</span><span class="sxs-lookup"><span data-stu-id="a410a-145">3600 - 36FF</span></span>  <br/> |<span data-ttu-id="a410a-146">フォルダーとアドレス帳のコンテナーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a410a-146">Folder and address book container properties</span></span>  <br/> |
|<span data-ttu-id="a410a-147">3700-38ff</span><span class="sxs-lookup"><span data-stu-id="a410a-147">3700 - 38FF</span></span>  <br/> |<span data-ttu-id="a410a-148">添付ファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a410a-148">Attachment properties</span></span>  <br/> |
|<span data-ttu-id="a410a-149">3900-39ff</span><span class="sxs-lookup"><span data-stu-id="a410a-149">3900 - 39FF</span></span>  <br/> |<span data-ttu-id="a410a-150">アドレス帳のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a410a-150">Address book properties</span></span>  <br/> |
|<span data-ttu-id="a410a-151">3a00-3BFF</span><span class="sxs-lookup"><span data-stu-id="a410a-151">3A00 - 3BFF</span></span>  <br/> |<span data-ttu-id="a410a-152">メッセージングユーザーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a410a-152">Messaging user properties</span></span>  <br/> |
|<span data-ttu-id="a410a-153">3c00-3c00</span><span class="sxs-lookup"><span data-stu-id="a410a-153">3C00 - 3CFF</span></span>  <br/> |<span data-ttu-id="a410a-154">配布リストのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a410a-154">Distribution list properties</span></span>  <br/> |
|<span data-ttu-id="a410a-155">3d00-3d00</span><span class="sxs-lookup"><span data-stu-id="a410a-155">3D00 - 3DFF</span></span>  <br/> |<span data-ttu-id="a410a-156">プロファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a410a-156">Profile properties</span></span>  <br/> |
|<span data-ttu-id="a410a-157">3e00-3fff</span><span class="sxs-lookup"><span data-stu-id="a410a-157">3E00 - 3FFF</span></span>  <br/> |<span data-ttu-id="a410a-158">状態オブジェクトのプロパティ</span><span class="sxs-lookup"><span data-stu-id="a410a-158">Status object properties</span></span>  <br/> |
   

