---
title: ストアの種類をプライベートプロパティに設定する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428544"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="eda4f-103">ストアの種類をプライベートプロパティに設定する</span><span class="sxs-lookup"><span data-stu-id="eda4f-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="eda4f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eda4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eda4f-105">セカンダリストアをプライベートとして扱います。</span><span class="sxs-lookup"><span data-stu-id="eda4f-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="eda4f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="eda4f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eda4f-107">公開:</span><span class="sxs-lookup"><span data-stu-id="eda4f-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="eda4f-108">[IMsgStore: imapiprop](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="eda4f-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="eda4f-109">作成者:</span><span class="sxs-lookup"><span data-stu-id="eda4f-109">Created by:</span></span>  <br/> |<span data-ttu-id="eda4f-110">ストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="eda4f-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="eda4f-111">アクセス先:</span><span class="sxs-lookup"><span data-stu-id="eda4f-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="eda4f-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="eda4f-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="eda4f-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="eda4f-113">Property type:</span></span>  <br/> |<span data-ttu-id="eda4f-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="eda4f-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="eda4f-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="eda4f-115">Access type:</span></span>  <br/> |<span data-ttu-id="eda4f-116">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="eda4f-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eda4f-117">注釈</span><span class="sxs-lookup"><span data-stu-id="eda4f-117">Remarks</span></span>

<span data-ttu-id="eda4f-118">ストアの機能を提供するには、ストアプロバイダーが[IMsgStore: imapiprop](imsgstoreimapiprop.md)を実装し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)呼び出しに渡されるこれらのプロパティに対して有効なプロパティタグを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="eda4f-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="eda4f-119">これらのプロパティのいずれかのプロパティタグが[imapiprop:: GetProps](imapiprop-getprops.md)に渡されると、ストアプロバイダーは、適切なプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="eda4f-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="eda4f-120">ストアプロバイダーは、 [hrgetoneprop](hrgetoneprop.md)および[hrgetoneprop](hrsetoneprop.md)を呼び出して、これらのプロパティを取得または設定できます。</span><span class="sxs-lookup"><span data-stu-id="eda4f-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="eda4f-121">このプロパティの値を取得するには、クライアントはまず[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を使用してプロパティタグを取得し、次に[imapiprop:: GetProps](imapiprop-getprops.md)でこのプロパティタグを指定して値を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eda4f-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="eda4f-122">[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)を呼び出す場合は、入力パラメーター _lpppropnames_でポイントされている[mapinameid](mapinameid.md)構造に次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="eda4f-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eda4f-123">lpguid:</span><span class="sxs-lookup"><span data-stu-id="eda4f-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="eda4f-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="eda4f-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="eda4f-125">ulkind:</span><span class="sxs-lookup"><span data-stu-id="eda4f-125">ulKind:</span></span>  <br/> |<span data-ttu-id="eda4f-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="eda4f-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="eda4f-127">種類が lpwstrname:</span><span class="sxs-lookup"><span data-stu-id="eda4f-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="eda4f-128">L "urn: スキーマ-microsoft-com: office: outlook # storetypeprivate"</span><span class="sxs-lookup"><span data-stu-id="eda4f-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="eda4f-129">ストアプロバイダーは、このプロパティを使用して、ユーザーのセカンダリストアである場合に、Outlook でこのプロパティをプライベートとして扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="eda4f-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="eda4f-130">既定では、Outlook は代理ストアと同じ方法でセカンダリストアを処理し、セカンダリストア内のアイテムはプライベートとしてマークされている場合にのみプライベートとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="eda4f-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="eda4f-131">このプロパティが**true**の場合、セカンダリストアから削除されたアイテムは、プライマリストアの [**削除済みアイテム**] フォルダーに移動されます。</span><span class="sxs-lookup"><span data-stu-id="eda4f-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="eda4f-132">親展とマークされたアイテムは表示されません。</span><span class="sxs-lookup"><span data-stu-id="eda4f-132">Items marked private are not displayed.</span></span> <span data-ttu-id="eda4f-133">下書きは、プライマリストアの [下書き] フォルダーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="eda4f-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="eda4f-134">outlook のバージョンが Microsoft Office Outlook 2003 Service Pack 1 より前の場合、またはその値が**false**の場合、このプロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="eda4f-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

