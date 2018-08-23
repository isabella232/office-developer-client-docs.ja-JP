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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cc8ff946081fb7817f0f6018acefbe31293a13a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581777"
---
# <a name="crawlsourcesupportmask"></a><span data-ttu-id="76345-103">CrawlSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="76345-103">CrawlSourceSupportMask</span></span>

  
  
<span data-ttu-id="76345-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76345-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76345-105">Microsoft Office Outlook では、ナビゲーション ウィンドウに表示する起動時に、連絡先、カレンダー、およびタスクのフォルダーを含むストア内のフォルダーをスキャンするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="76345-105">Specifies whether Microsoft Office Outlook should scan folders in a store, including Contacts, Calendar, and Tasks folders, on startup to populate the Navigation Pane.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="76345-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="76345-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76345-107">公開されます。</span><span class="sxs-lookup"><span data-stu-id="76345-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="76345-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="76345-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="76345-109">によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="76345-109">Created by:</span></span>  <br/> |<span data-ttu-id="76345-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="76345-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="76345-111">によってアクセスします。</span><span class="sxs-lookup"><span data-stu-id="76345-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="76345-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="76345-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="76345-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="76345-113">Property type:</span></span>  <br/> |<span data-ttu-id="76345-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="76345-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="76345-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="76345-115">Access type:</span></span>  <br/> |<span data-ttu-id="76345-116">読み取り専用または読み取り/書き込みによってストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="76345-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76345-117">注釈</span><span class="sxs-lookup"><span data-stu-id="76345-117">Remarks</span></span>

<span data-ttu-id="76345-118">ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。</span><span class="sxs-lookup"><span data-stu-id="76345-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="76345-119">これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="76345-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="76345-120">ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="76345-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="76345-121">このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76345-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="76345-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="76345-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76345-123">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="76345-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="76345-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="76345-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="76345-125">ulKind。</span><span class="sxs-lookup"><span data-stu-id="76345-125">ulKind:</span></span>  <br/> |<span data-ttu-id="76345-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="76345-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="76345-127">Kind.lpwstrName。</span><span class="sxs-lookup"><span data-stu-id="76345-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="76345-128">L"CrawlSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="76345-128">L"CrawlSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="76345-129">このプロパティは、Outlook がストア内のさまざまなフォルダーをスキャンするかどうかを指定するのには、ストア プロバイダーの方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="76345-129">This property provides a way for store providers to specify whether Outlook should scan various folders in a store.</span></span> <span data-ttu-id="76345-130">Outlook は、**ナビゲーション**ウィンドウを設定するのには開かれている各ストアで既存のフォルダーをスキャンする場合の起動時に使用されます。Outlook は、スキャンを開始する前に存在し、ストアでは、このプロパティの値をチェックします。</span><span class="sxs-lookup"><span data-stu-id="76345-130">It is used on startup when Outlook scans existing folders on each opened store to populate the **Navigation** pane; Outlook checks for the presence and value of this property on a store before initiating the scan.</span></span> 
  
<span data-ttu-id="76345-131">既定では、このプロパティは、ストアは、Outlook は、ストア上のフォルダーをスキャンできることを意味では公開されません。</span><span class="sxs-lookup"><span data-stu-id="76345-131">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="76345-132">プロパティが公開されている場合、値は次のことです。</span><span class="sxs-lookup"><span data-stu-id="76345-132">If the property is exposed, the following are the possible values:</span></span>
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="76345-133">CSM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="76345-133">CSM_DEFAULT</span></span>
  
- <span data-ttu-id="76345-134">Outlook では、ストア上のフォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="76345-134">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="76345-135">CSM_DO_NOT_CRAWL</span><span class="sxs-lookup"><span data-stu-id="76345-135">CSM_DO_NOT_CRAWL</span></span>
  
- <span data-ttu-id="76345-136">Outlook では、ストア上のフォルダーをスキャンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="76345-136">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="76345-137">CSM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="76345-137">CSM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="76345-138">ストア内のこのプロパティを変更するクライアントを許可しません。</span><span class="sxs-lookup"><span data-stu-id="76345-138">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="76345-139">定数**CSM_CLIENT_DO_NOT_CHANGE**は、将来の参照と、現在実装されていません注意してください。</span><span class="sxs-lookup"><span data-stu-id="76345-139">Note that the constant **CSM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="76345-140">ここでは、ストアは、このプロパティでストアから返される値をハードコーディングするで、このフラグを変更することからクライアントを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="76345-140">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

