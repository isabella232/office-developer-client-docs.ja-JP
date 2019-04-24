---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281593"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="2f035-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="2f035-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="2f035-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f035-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f035-105">Microsoft Office Outlook がストア内のフォルダーをスキャンして、それらを自動的にアーカイブするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2f035-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2f035-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2f035-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f035-107">公開:</span><span class="sxs-lookup"><span data-stu-id="2f035-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="2f035-108">[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2f035-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="2f035-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="2f035-109">Created by:</span></span>  <br/> |<span data-ttu-id="2f035-110">ストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="2f035-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="2f035-111">アクセス先:</span><span class="sxs-lookup"><span data-stu-id="2f035-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="2f035-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="2f035-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="2f035-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="2f035-113">Property type:</span></span>  <br/> |<span data-ttu-id="2f035-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2f035-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2f035-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="2f035-115">Access type:</span></span>  <br/> |<span data-ttu-id="2f035-116">ストアプロバイダーに応じて読み取り専用または読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="2f035-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f035-117">解説</span><span class="sxs-lookup"><span data-stu-id="2f035-117">Remarks</span></span>

<span data-ttu-id="2f035-118">ストアの機能を提供するには、ストアプロバイダーが[imapiprop: IUnknown](imapipropiunknown.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f035-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="2f035-119">これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f035-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="2f035-120">ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="2f035-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="2f035-121">このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f035-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="2f035-122">[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2f035-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f035-123">lpguid:</span><span class="sxs-lookup"><span data-stu-id="2f035-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="2f035-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2f035-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2f035-125">ulkind:</span><span class="sxs-lookup"><span data-stu-id="2f035-125">ulKind:</span></span>  <br/> |<span data-ttu-id="2f035-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="2f035-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="2f035-127">種類が lpwstrname:</span><span class="sxs-lookup"><span data-stu-id="2f035-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="2f035-128">L "ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="2f035-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="2f035-129">このプロパティを使用すると、Outlook がストア内のフォルダーをスキャンして、それらを自動的にアーカイブするかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="2f035-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="2f035-130">既定では、このプロパティはストアに公開されていないため、Outlook はストアのフォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="2f035-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="2f035-131">プロパティが公開されている場合は、次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="2f035-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="2f035-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2f035-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="2f035-133">Outlook は、ストア上のフォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="2f035-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="2f035-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="2f035-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="2f035-135">Outlook は、ストア上のフォルダーをスキャンしません。</span><span class="sxs-lookup"><span data-stu-id="2f035-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="2f035-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="2f035-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="2f035-137">クライアントがストアでこのプロパティを変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="2f035-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="2f035-138">定数**ASM_CLIENT_DO_NOT_CHANGE**は将来の参照用であり、現在は実装されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2f035-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="2f035-139">この時点で、ストアは、このプロパティに対してストアが返す値をハードコーディングすることにより、クライアントがこのフラグを変更できないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f035-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

