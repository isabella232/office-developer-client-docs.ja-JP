---
title: プロパティ識別子の範囲
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422706"
---
# <a name="property-identifier-ranges"></a><span data-ttu-id="ca19b-103">プロパティ識別子の範囲</span><span class="sxs-lookup"><span data-stu-id="ca19b-103">Property Identifier Ranges</span></span>

  
  
<span data-ttu-id="ca19b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca19b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca19b-105">次の表は、各範囲のプロパティの所有者を示す、プロパティ識別子の異なる範囲の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="ca19b-105">The following table summarizes the different ranges for property identifiers, describing the owner for the properties in each range.</span></span>
  
|<span data-ttu-id="ca19b-106">**識別子の範囲**</span><span class="sxs-lookup"><span data-stu-id="ca19b-106">**Identifier range**</span></span>|<span data-ttu-id="ca19b-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="ca19b-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca19b-108">0000</span><span class="sxs-lookup"><span data-stu-id="ca19b-108">0000</span></span>  <br/> |<span data-ttu-id="ca19b-109">特別な値を使用して MAPI によって **予約** PR_NULL。</span><span class="sxs-lookup"><span data-stu-id="ca19b-109">Reserved by MAPI for the special value **PR_NULL**.</span></span>  <br/> |
|<span data-ttu-id="ca19b-110">0001 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-110">0001 - 0BFF</span></span>  <br/> |<span data-ttu-id="ca19b-111">MAPI で定義されたメッセージ エンベロープ プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-111">Message envelope properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ca19b-112">0C00 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-112">0C00 - 0DFF</span></span>  <br/> |<span data-ttu-id="ca19b-113">MAPI によって定義された受信者プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-113">Recipient properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ca19b-114">0E00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-114">0E00 - 0FFF</span></span>  <br/> |<span data-ttu-id="ca19b-115">MAPI によって定義された送信不可のメッセージ プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-115">Non-transmittable message properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ca19b-116">1000 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-116">1000 - 2FFF</span></span>  <br/> |<span data-ttu-id="ca19b-117">MAPI によって定義されたメッセージ コンテンツ プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-117">Message content properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ca19b-118">3000 - 3FFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-118">3000 - 3FFF</span></span>  <br/> |<span data-ttu-id="ca19b-119">MAPI によって定義されたメッセージおよび受信者以外のオブジェクトのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-119">Properties for objects other than messages and recipients defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ca19b-120">4000 ~ 57FF</span><span class="sxs-lookup"><span data-stu-id="ca19b-120">4000 - 57FF</span></span>  <br/> |<span data-ttu-id="ca19b-121">トランスポート プロバイダーによって定義されるメッセージ エンベロープ プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-121">Message envelope properties defined by transport providers.</span></span>  <br/> |
|<span data-ttu-id="ca19b-122">5800 - 5FFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-122">5800 - 5FFF</span></span>  <br/> |<span data-ttu-id="ca19b-123">トランスポート プロバイダーとアドレス帳プロバイダーによって定義される受信者プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-123">Recipient properties defined by transport and address book providers.</span></span>  <br/> |
|<span data-ttu-id="ca19b-124">6000 ~ 65FF</span><span class="sxs-lookup"><span data-stu-id="ca19b-124">6000 - 65FF</span></span>  <br/> |<span data-ttu-id="ca19b-125">クライアントによって定義された送信不可のメッセージ プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-125">Non-transmittable message properties defined by clients.</span></span>  <br/> |
|<span data-ttu-id="ca19b-126">6600 - 67FF</span><span class="sxs-lookup"><span data-stu-id="ca19b-126">6600 - 67FF</span></span>  <br/> |<span data-ttu-id="ca19b-127">サービス プロバイダーによって定義された送信不可のプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-127">Non-transmittable properties defined by a service provider.</span></span> <span data-ttu-id="ca19b-128">これらのプロパティは、ユーザーに表示または非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ca19b-128">These properties can be visible or invisible to users.</span></span>  <br/> |
|<span data-ttu-id="ca19b-129">6800 - 7BFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-129">6800 - 7BFF</span></span>  <br/> |<span data-ttu-id="ca19b-130">これらのクラスの作成者によって定義されたカスタム メッセージ クラスのメッセージ コンテンツ プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-130">Message content properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="ca19b-131">7C00 - 7FFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-131">7C00 - 7FFF</span></span>  <br/> |<span data-ttu-id="ca19b-132">これらのクラスの作成者によって定義されたカスタム メッセージ クラスの送信不可プロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-132">Non-transmittable properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="ca19b-133">8000 - FFFE</span><span class="sxs-lookup"><span data-stu-id="ca19b-133">8000 - FFFE</span></span>  <br/> |<span data-ttu-id="ca19b-134">[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)および[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを使用して名前で識別されるクライアントおよび場合によってはサービス プロバイダーによって定義されるプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ca19b-134">Properties defined by clients and occasionally service providers that are identified by name through the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span>  <br/> |
|<span data-ttu-id="ca19b-135">FFFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-135">FFFF</span></span>  <br/> |<span data-ttu-id="ca19b-136">特別なエラー値を使用して MAPI によって予約PROP_ID_INVALID。</span><span class="sxs-lookup"><span data-stu-id="ca19b-136">Reserved by MAPI for the special error value PROP_ID_INVALID.</span></span>  <br/> |
   
<span data-ttu-id="ca19b-137">3000 ~ 3FFF の範囲は、メッセージまたは受信者に関連しないプロパティ用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="ca19b-137">The range between 3000 and 3FFF is reserved for properties that are not related to either messages or recipients.</span></span> <span data-ttu-id="ca19b-138">MAPI は、この範囲をオブジェクトの種類によってサブ範囲に分割します。次の表に、この詳細な内訳を示します。</span><span class="sxs-lookup"><span data-stu-id="ca19b-138">MAPI divides this range into sub-ranges by types of object; the following table shows this further breakdown.</span></span> 
  
|<span data-ttu-id="ca19b-139">**識別子の範囲**</span><span class="sxs-lookup"><span data-stu-id="ca19b-139">**Identifier range**</span></span>|<span data-ttu-id="ca19b-140">**プロパティの種類**</span><span class="sxs-lookup"><span data-stu-id="ca19b-140">**Type of property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca19b-141">3000 ~ 33FF</span><span class="sxs-lookup"><span data-stu-id="ca19b-141">3000 - 33FF</span></span>  <br/> |<span data-ttu-id="ca19b-142">複数のオブジェクトに表示される一般的なプロパティ (PR_DISPLAY_NAME、PR_ENTRYID)。  </span><span class="sxs-lookup"><span data-stu-id="ca19b-142">Common properties that appear on multiple objects, such as **PR_DISPLAY_NAME** and **PR_ENTRYID**.</span></span>  <br/> |
|<span data-ttu-id="ca19b-143">3400 ~ 35FF</span><span class="sxs-lookup"><span data-stu-id="ca19b-143">3400 - 35FF</span></span>  <br/> |<span data-ttu-id="ca19b-144">メッセージ ストアのプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca19b-144">Message store properties</span></span>  <br/> |
|<span data-ttu-id="ca19b-145">3600 ~ 36FF</span><span class="sxs-lookup"><span data-stu-id="ca19b-145">3600 - 36FF</span></span>  <br/> |<span data-ttu-id="ca19b-146">フォルダーとアドレス帳コンテナーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca19b-146">Folder and address book container properties</span></span>  <br/> |
|<span data-ttu-id="ca19b-147">3700 - 38FF</span><span class="sxs-lookup"><span data-stu-id="ca19b-147">3700 - 38FF</span></span>  <br/> |<span data-ttu-id="ca19b-148">添付ファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca19b-148">Attachment properties</span></span>  <br/> |
|<span data-ttu-id="ca19b-149">3900 - 39FF</span><span class="sxs-lookup"><span data-stu-id="ca19b-149">3900 - 39FF</span></span>  <br/> |<span data-ttu-id="ca19b-150">アドレス帳のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca19b-150">Address book properties</span></span>  <br/> |
|<span data-ttu-id="ca19b-151">3A00 - 3BFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-151">3A00 - 3BFF</span></span>  <br/> |<span data-ttu-id="ca19b-152">メッセージング ユーザーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca19b-152">Messaging user properties</span></span>  <br/> |
|<span data-ttu-id="ca19b-153">3C00 - 3CFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-153">3C00 - 3CFF</span></span>  <br/> |<span data-ttu-id="ca19b-154">配布リストのプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca19b-154">Distribution list properties</span></span>  <br/> |
|<span data-ttu-id="ca19b-155">3D00 - 3DFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-155">3D00 - 3DFF</span></span>  <br/> |<span data-ttu-id="ca19b-156">プロファイル プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca19b-156">Profile properties</span></span>  <br/> |
|<span data-ttu-id="ca19b-157">3E00 - 3FFF</span><span class="sxs-lookup"><span data-stu-id="ca19b-157">3E00 - 3FFF</span></span>  <br/> |<span data-ttu-id="ca19b-158">Status オブジェクトのプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca19b-158">Status object properties</span></span>  <br/> |
   

