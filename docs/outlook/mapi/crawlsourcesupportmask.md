---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420914"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="3ec7e-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="3ec7e-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="3ec7e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ec7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ec7e-105">Microsoft Office Outlook で、連絡先、予定表、タスクフォルダーなどのストア内のフォルダーをスキャンして、ナビゲーションウィンドウに設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3ec7e-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3ec7e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ec7e-107">公開:</span><span class="sxs-lookup"><span data-stu-id="3ec7e-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="3ec7e-108">[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3ec7e-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="3ec7e-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="3ec7e-109">Created by:</span></span>  <br/> |<span data-ttu-id="3ec7e-110">ストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="3ec7e-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="3ec7e-111">アクセス先:</span><span class="sxs-lookup"><span data-stu-id="3ec7e-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="3ec7e-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="3ec7e-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="3ec7e-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="3ec7e-113">Property type:</span></span>  <br/> |<span data-ttu-id="3ec7e-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3ec7e-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3ec7e-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="3ec7e-115">Access type:</span></span>  <br/> |<span data-ttu-id="3ec7e-116">ストアプロバイダーに応じて読み取り専用または読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="3ec7e-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ec7e-117">注釈</span><span class="sxs-lookup"><span data-stu-id="3ec7e-117">Remarks</span></span>

<span data-ttu-id="3ec7e-118">ストアの機能を提供するには、ストアプロバイダーが[imapiprop: IUnknown](imapipropiunknown.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="3ec7e-119">これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="3ec7e-120">ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="3ec7e-121">このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="3ec7e-122">[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ec7e-123">lpguid:</span><span class="sxs-lookup"><span data-stu-id="3ec7e-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="3ec7e-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="3ec7e-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="3ec7e-125">ulkind:</span><span class="sxs-lookup"><span data-stu-id="3ec7e-125">ulKind:</span></span>  <br/> |<span data-ttu-id="3ec7e-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="3ec7e-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="3ec7e-127">種類が lpwstrname:</span><span class="sxs-lookup"><span data-stu-id="3ec7e-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="3ec7e-128">L "CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="3ec7e-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="3ec7e-129">このプロパティは、Outlook がストア内のさまざまなフォルダーをスキャンする必要があるかどうかを、ストアプロバイダーが指定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="3ec7e-130">これは、Outlook が開いている各ストアの既存のフォルダーをスキャンして**ナビゲーション**ウィンドウにデータを設定するときに使用されます。Outlook は、スキャンを開始する前に、ストアでこのプロパティのプレゼンスと値をチェックします。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="3ec7e-131">既定では、このプロパティはストアに公開されていないため、Outlook はストアのフォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="3ec7e-132">プロパティが公開されている場合は、次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="3ec7e-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3ec7e-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="3ec7e-134">Outlook は、ストア上のフォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="3ec7e-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="3ec7e-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="3ec7e-136">Outlook は、ストア上のフォルダーをスキャンしません。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="3ec7e-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="3ec7e-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="3ec7e-138">クライアントがストアでこのプロパティを変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="3ec7e-139">定数**CSM_CLIENT_DO_NOT_CHANGE**は将来の参照用であり、現在は実装されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="3ec7e-140">この時点で、ストアは、このプロパティに対してストアが返す値をハードコーディングすることにより、クライアントがこのフラグを変更できないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="3ec7e-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

