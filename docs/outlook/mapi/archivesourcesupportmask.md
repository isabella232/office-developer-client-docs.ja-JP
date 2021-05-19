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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418093"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="e34ef-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="e34ef-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="e34ef-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e34ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e34ef-105">ストア内のMicrosoft Office Outlookをスキャンして自動的にアーカイブするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e34ef-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e34ef-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e34ef-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e34ef-107">次の場合に公開されます。</span><span class="sxs-lookup"><span data-stu-id="e34ef-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="e34ef-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) オブジェクト</span><span class="sxs-lookup"><span data-stu-id="e34ef-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="e34ef-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="e34ef-109">Created by:</span></span>  <br/> |<span data-ttu-id="e34ef-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e34ef-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="e34ef-111">アクセス者:</span><span class="sxs-lookup"><span data-stu-id="e34ef-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="e34ef-112">Outlookクライアント</span><span class="sxs-lookup"><span data-stu-id="e34ef-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="e34ef-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="e34ef-113">Property type:</span></span>  <br/> |<span data-ttu-id="e34ef-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e34ef-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e34ef-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="e34ef-115">Access type:</span></span>  <br/> |<span data-ttu-id="e34ef-116">ストア プロバイダーに応じて読み取り専用または読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e34ef-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e34ef-117">注釈</span><span class="sxs-lookup"><span data-stu-id="e34ef-117">Remarks</span></span>

<span data-ttu-id="e34ef-118">ストア機能を提供するには、ストア プロバイダーが [IMAPIProp : IUnknown](imapipropiunknown.md) を実装し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) 呼び出しに渡されるこれらのプロパティの有効なプロパティ タグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e34ef-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="e34ef-119">これらのプロパティのプロパティ タグが [IMAPIProp::GetProps](imapiprop-getprops.md)に渡される場合、ストア プロバイダーは正しいプロパティ値も返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e34ef-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="e34ef-120">ストア プロバイダーは [、HrGetOneProp](hrgetoneprop.md) と [HrSetOneProp](hrsetoneprop.md) を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="e34ef-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="e34ef-121">このプロパティの値を取得するには、まず [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) を使用してプロパティ タグを取得し [、IMAPIProp::GetProps](imapiprop-getprops.md) でこのプロパティ タグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e34ef-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="e34ef-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lppPropNames_ が指す [MAPINAMEID](mapinameid.md)構造体に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e34ef-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e34ef-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="e34ef-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="e34ef-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e34ef-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e34ef-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="e34ef-125">ulKind:</span></span>  <br/> |<span data-ttu-id="e34ef-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="e34ef-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="e34ef-127">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="e34ef-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="e34ef-128">L"ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="e34ef-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="e34ef-129">このプロパティを使用すると、ストア プロバイダーは、Outlookフォルダーをスキャンして自動的にアーカイブするかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="e34ef-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="e34ef-130">既定では、このプロパティはストアで公開されません。つまり、Outlookフォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="e34ef-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="e34ef-131">プロパティが公開されている場合は、次の値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e34ef-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="e34ef-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="e34ef-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="e34ef-133">Outlookストア上のフォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="e34ef-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="e34ef-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="e34ef-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="e34ef-135">Outlookフォルダーをスキャンしない必要があります。</span><span class="sxs-lookup"><span data-stu-id="e34ef-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="e34ef-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="e34ef-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="e34ef-137">クライアントがストアでこのプロパティを変更を許可しない。</span><span class="sxs-lookup"><span data-stu-id="e34ef-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="e34ef-138">定数の値は **ASM_CLIENT_DO_NOT_CHANGE** 参照用であり、現在実装されていません。</span><span class="sxs-lookup"><span data-stu-id="e34ef-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="e34ef-139">今のところ、ストアは、このプロパティに対してストアが返す値をハードコードすることで、クライアントがこのフラグを変更できません。</span><span class="sxs-lookup"><span data-stu-id="e34ef-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

