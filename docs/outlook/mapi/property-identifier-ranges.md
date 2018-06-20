---
title: プロパティ識別子の範囲
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aee199cbbd05606d20378023f103fa122f1457f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803697"
---
# <a name="property-identifier-ranges"></a><span data-ttu-id="41352-103">プロパティ識別子の範囲</span><span class="sxs-lookup"><span data-stu-id="41352-103">Property Identifier Ranges</span></span>

  
  
<span data-ttu-id="41352-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41352-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41352-105">次の表は、それぞれの範囲内のプロパティの所有者を示すプロパティ識別子のさまざまな範囲をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="41352-105">The following table summarizes the different ranges for property identifiers, describing the owner for the properties in each range.</span></span>
  
|<span data-ttu-id="41352-106">**識別子の範囲**</span><span class="sxs-lookup"><span data-stu-id="41352-106">**Identifier range**</span></span>|<span data-ttu-id="41352-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="41352-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41352-108">0000</span><span class="sxs-lookup"><span data-stu-id="41352-108">0000</span></span>  <br/> |<span data-ttu-id="41352-109">特別な値**PR_NULL**MAPI によって予約されています。</span><span class="sxs-lookup"><span data-stu-id="41352-109">Reserved by MAPI for the special value **PR_NULL**.</span></span>  <br/> |
|<span data-ttu-id="41352-110">0001-0BFF</span><span class="sxs-lookup"><span data-stu-id="41352-110">0001 - 0BFF</span></span>  <br/> |<span data-ttu-id="41352-111">メッセージ エンベロープのプロパティは MAPI によって定義されています。</span><span class="sxs-lookup"><span data-stu-id="41352-111">Message envelope properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="41352-112">0C 00 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="41352-112">0C00 - 0DFF</span></span>  <br/> |<span data-ttu-id="41352-113">MAPI によって定義されている受信者のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="41352-113">Recipient properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="41352-114">0E00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="41352-114">0E00 - 0FFF</span></span>  <br/> |<span data-ttu-id="41352-115">非送信できるメッセージのプロパティが MAPI によって定義されています。</span><span class="sxs-lookup"><span data-stu-id="41352-115">Non-transmittable message properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="41352-116">1000-2FFF</span><span class="sxs-lookup"><span data-stu-id="41352-116">1000 - 2FFF</span></span>  <br/> |<span data-ttu-id="41352-117">メッセージのコンテンツ プロパティが MAPI によって定義されています。</span><span class="sxs-lookup"><span data-stu-id="41352-117">Message content properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="41352-118">3000-3FFF</span><span class="sxs-lookup"><span data-stu-id="41352-118">3000 - 3FFF</span></span>  <br/> |<span data-ttu-id="41352-119">メッセージと受信者が MAPI によって定義されている以外のオブジェクトのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="41352-119">Properties for objects other than messages and recipients defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="41352-120">4000-57FF</span><span class="sxs-lookup"><span data-stu-id="41352-120">4000 - 57FF</span></span>  <br/> |<span data-ttu-id="41352-121">トランスポート プロバイダーによって定義されているメッセージ エンベロープのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="41352-121">Message envelope properties defined by transport providers.</span></span>  <br/> |
|<span data-ttu-id="41352-122">5800-5FFF</span><span class="sxs-lookup"><span data-stu-id="41352-122">5800 - 5FFF</span></span>  <br/> |<span data-ttu-id="41352-123">トランスポートとアドレス帳のプロバイダーで定義されている受信者のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="41352-123">Recipient properties defined by transport and address book providers.</span></span>  <br/> |
|<span data-ttu-id="41352-124">6000-65FF</span><span class="sxs-lookup"><span data-stu-id="41352-124">6000 - 65FF</span></span>  <br/> |<span data-ttu-id="41352-125">非送信できるメッセージのプロパティがクライアントによって定義されています。</span><span class="sxs-lookup"><span data-stu-id="41352-125">Non-transmittable message properties defined by clients.</span></span>  <br/> |
|<span data-ttu-id="41352-126">6600-67FF</span><span class="sxs-lookup"><span data-stu-id="41352-126">6600 - 67FF</span></span>  <br/> |<span data-ttu-id="41352-127">サービス プロバイダーによって定義されているプロパティの非送信できます。</span><span class="sxs-lookup"><span data-stu-id="41352-127">Non-transmittable properties defined by a service provider.</span></span> <span data-ttu-id="41352-128">これらのプロパティは、表示または非表示をするユーザーにします。</span><span class="sxs-lookup"><span data-stu-id="41352-128">These properties can be visible or invisible to users.</span></span>  <br/> |
|<span data-ttu-id="41352-129">6800-7BFF</span><span class="sxs-lookup"><span data-stu-id="41352-129">6800 - 7BFF</span></span>  <br/> |<span data-ttu-id="41352-130">これらのクラスの作成者が定義されているカスタム メッセージ クラスのメッセージ コンテンツのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="41352-130">Message content properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="41352-131">7C 00 - 7 FFF</span><span class="sxs-lookup"><span data-stu-id="41352-131">7C00 - 7FFF</span></span>  <br/> |<span data-ttu-id="41352-132">カスタム メッセージ クラスがそのクラスの作成者が定義されている以外の転送が可能なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="41352-132">Non-transmittable properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="41352-133">8000-FFFE になります</span><span class="sxs-lookup"><span data-stu-id="41352-133">8000 - FFFE</span></span>  <br/> |<span data-ttu-id="41352-134">プロパティは、クライアントによって定義され、サービス ・ プロバイダーの[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドと[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを名前で識別される場合があります。</span><span class="sxs-lookup"><span data-stu-id="41352-134">Properties defined by clients and occasionally service providers that are identified by name through the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span>  <br/> |
|<span data-ttu-id="41352-135">FFFF</span><span class="sxs-lookup"><span data-stu-id="41352-135">FFFF</span></span>  <br/> |<span data-ttu-id="41352-136">特殊なエラー値 PROP_ID_INVALID MAPI によって予約されています。</span><span class="sxs-lookup"><span data-stu-id="41352-136">Reserved by MAPI for the special error value PROP_ID_INVALID.</span></span>  <br/> |
   
<span data-ttu-id="41352-137">3000 の間の範囲 3FFF はメッセージまたは受信者のいずれかに関連付けられていないプロパティ用に予約されているとします。</span><span class="sxs-lookup"><span data-stu-id="41352-137">The range between 3000 and 3FFF is reserved for properties that are not related to either messages or recipients.</span></span> <span data-ttu-id="41352-138">MAPI のサブ範囲にオブジェクトの種類でこの範囲を分割します。次の表は、このさらなる内訳を示しています。</span><span class="sxs-lookup"><span data-stu-id="41352-138">MAPI divides this range into sub-ranges by types of object; the following table shows this further breakdown.</span></span> 
  
|<span data-ttu-id="41352-139">**識別子の範囲**</span><span class="sxs-lookup"><span data-stu-id="41352-139">**Identifier range**</span></span>|<span data-ttu-id="41352-140">**プロパティの型**</span><span class="sxs-lookup"><span data-stu-id="41352-140">**Type of property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41352-141">3000-33FF</span><span class="sxs-lookup"><span data-stu-id="41352-141">3000 - 33FF</span></span>  <br/> |<span data-ttu-id="41352-142">**PR_DISPLAY_NAME**や**PR_ENTRYID**など、複数のオブジェクト上に表示される一般的なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="41352-142">Common properties that appear on multiple objects, such as **PR_DISPLAY_NAME** and **PR_ENTRYID**.</span></span>  <br/> |
|<span data-ttu-id="41352-143">3400-35FF</span><span class="sxs-lookup"><span data-stu-id="41352-143">3400 - 35FF</span></span>  <br/> |<span data-ttu-id="41352-144">メッセージ ・ ストア ・ プロパティ</span><span class="sxs-lookup"><span data-stu-id="41352-144">Message store properties</span></span>  <br/> |
|<span data-ttu-id="41352-145">3600-36FF</span><span class="sxs-lookup"><span data-stu-id="41352-145">3600 - 36FF</span></span>  <br/> |<span data-ttu-id="41352-146">フォルダーとアドレス帳コンテナーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="41352-146">Folder and address book container properties</span></span>  <br/> |
|<span data-ttu-id="41352-147">3700-38FF</span><span class="sxs-lookup"><span data-stu-id="41352-147">3700 - 38FF</span></span>  <br/> |<span data-ttu-id="41352-148">添付ファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="41352-148">Attachment properties</span></span>  <br/> |
|<span data-ttu-id="41352-149">3900-39FF</span><span class="sxs-lookup"><span data-stu-id="41352-149">3900 - 39FF</span></span>  <br/> |<span data-ttu-id="41352-150">アドレス帳のプロパティ</span><span class="sxs-lookup"><span data-stu-id="41352-150">Address book properties</span></span>  <br/> |
|<span data-ttu-id="41352-151">3A00 - 3BFF</span><span class="sxs-lookup"><span data-stu-id="41352-151">3A00 - 3BFF</span></span>  <br/> |<span data-ttu-id="41352-152">メッセージング ユーザーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="41352-152">Messaging user properties</span></span>  <br/> |
|<span data-ttu-id="41352-153">3C 00 - 3CFF</span><span class="sxs-lookup"><span data-stu-id="41352-153">3C00 - 3CFF</span></span>  <br/> |<span data-ttu-id="41352-154">配布リストのプロパティ</span><span class="sxs-lookup"><span data-stu-id="41352-154">Distribution list properties</span></span>  <br/> |
|<span data-ttu-id="41352-155">3D 00 - 3DFF</span><span class="sxs-lookup"><span data-stu-id="41352-155">3D00 - 3DFF</span></span>  <br/> |<span data-ttu-id="41352-156">プロファイルのプロパティ</span><span class="sxs-lookup"><span data-stu-id="41352-156">Profile properties</span></span>  <br/> |
|<span data-ttu-id="41352-157">3E00 - 3FFF</span><span class="sxs-lookup"><span data-stu-id="41352-157">3E00 - 3FFF</span></span>  <br/> |<span data-ttu-id="41352-158">ステータス オブジェクトのプロパティ</span><span class="sxs-lookup"><span data-stu-id="41352-158">Status object properties</span></span>  <br/> |
   

