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
ms.openlocfilehash: 1e0c099783b4d44b1aaf746b07c77981c135ca9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19799687"
---
# <a name="archivesourcesupportmask"></a><span data-ttu-id="31724-103">ArchiveSourceSupportMask</span><span class="sxs-lookup"><span data-stu-id="31724-103">ArchiveSourceSupportMask</span></span>

  
  
<span data-ttu-id="31724-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31724-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31724-105">Microsoft Office Outlook がストア内のフォルダーをスキャンし、自動的にアーカイブしてかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="31724-105">Specifies whether Microsoft Office Outlook should scan folders in a store and archive them automatically.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="31724-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="31724-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31724-107">公開されます。</span><span class="sxs-lookup"><span data-stu-id="31724-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="31724-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="31724-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="31724-109">によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="31724-109">Created by:</span></span>  <br/> |<span data-ttu-id="31724-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="31724-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="31724-111">によってアクセスします。</span><span class="sxs-lookup"><span data-stu-id="31724-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="31724-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="31724-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="31724-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="31724-113">Property type:</span></span>  <br/> |<span data-ttu-id="31724-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="31724-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="31724-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="31724-115">Access type:</span></span>  <br/> |<span data-ttu-id="31724-116">読み取り専用または読み取り/書き込みによってストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="31724-116">Read-only or read/write depending on the store provider</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31724-117">注釈</span><span class="sxs-lookup"><span data-stu-id="31724-117">Remarks</span></span>

<span data-ttu-id="31724-118">ストア機能を提供するストア プロバイダーを実装する必要があります[IMAPIProp: IUnknown](imapipropiunknown.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。</span><span class="sxs-lookup"><span data-stu-id="31724-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="31724-119">これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="31724-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="31724-120">ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="31724-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="31724-121">このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31724-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="31724-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="31724-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31724-123">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="31724-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="31724-124">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="31724-124">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="31724-125">ulKind。</span><span class="sxs-lookup"><span data-stu-id="31724-125">ulKind:</span></span>  <br/> |<span data-ttu-id="31724-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="31724-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="31724-127">Kind.lpwstrName。</span><span class="sxs-lookup"><span data-stu-id="31724-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="31724-128">L"ArchiveSourceSupportMask"</span><span class="sxs-lookup"><span data-stu-id="31724-128">L"ArchiveSourceSupportMask"</span></span>  <br/> |
   
<span data-ttu-id="31724-129">このプロパティは、Outlook がストア内のフォルダーをスキャンし、自動的にアーカイブしているかどうかを指定するのには、ストア プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="31724-129">This property allows store providers to specify whether Outlook should scan folders in a store and archive them automatically.</span></span>
  
<span data-ttu-id="31724-130">既定では、このプロパティは、ストアは、Outlook は、ストア上のフォルダーをスキャンできることを意味では公開されません。</span><span class="sxs-lookup"><span data-stu-id="31724-130">By default, this property is not exposed on a store, which means Outlook can scan folders on the store.</span></span> <span data-ttu-id="31724-131">プロパティが公開されている場合、値は次のことです。</span><span class="sxs-lookup"><span data-stu-id="31724-131">If the property is exposed, the following are the possible values:</span></span>
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

<span data-ttu-id="31724-132">ASM_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="31724-132">ASM_DEFAULT</span></span>
  
- <span data-ttu-id="31724-133">Outlook では、ストア上のフォルダーをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="31724-133">Outlook can scan folders on the store.</span></span>
    
<span data-ttu-id="31724-134">ASM_DO_NOT_ARCHIVE</span><span class="sxs-lookup"><span data-stu-id="31724-134">ASM_DO_NOT_ARCHIVE</span></span>
  
- <span data-ttu-id="31724-135">Outlook では、ストア上のフォルダーをスキャンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31724-135">Outlook should not scan folders on the store.</span></span>
    
<span data-ttu-id="31724-136">ASM_CLIENT_DO_NOT_CHANGE</span><span class="sxs-lookup"><span data-stu-id="31724-136">ASM_CLIENT_DO_NOT_CHANGE</span></span>
  
- <span data-ttu-id="31724-137">ストア内のこのプロパティを変更するクライアントを許可しません。</span><span class="sxs-lookup"><span data-stu-id="31724-137">Do not allow clients to change this property on the store.</span></span> <span data-ttu-id="31724-138">定数**ASM_CLIENT_DO_NOT_CHANGE**は、将来の参照と、現在実装されていません注意してください。</span><span class="sxs-lookup"><span data-stu-id="31724-138">Note that the constant **ASM_CLIENT_DO_NOT_CHANGE** is for future reference and is not currently implemented.</span></span> <span data-ttu-id="31724-139">ここでは、ストアは、このプロパティでストアから返される値をハードコーディングするで、このフラグを変更することからクライアントを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="31724-139">For now, a store can prevent clients from changing this flag by hardcoding the value that the store returns for this property.</span></span> 
    

