---
title: ストアの種類をプライベート プロパティにする
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f60d9524af18bb7f2e876386c45b84f207d42bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801314"
---
# <a name="make-store-type-private-property"></a><span data-ttu-id="61e89-103">ストアの種類をプライベート プロパティにする</span><span class="sxs-lookup"><span data-stu-id="61e89-103">Make Store Type Private Property</span></span>

  
  
<span data-ttu-id="61e89-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61e89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61e89-105">セカンダリ ・ ストアは、プライベートとして扱います。</span><span class="sxs-lookup"><span data-stu-id="61e89-105">Treats a secondary store as private.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="61e89-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="61e89-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61e89-107">公開されます。</span><span class="sxs-lookup"><span data-stu-id="61e89-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="61e89-108">[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)オブジェクト</span><span class="sxs-lookup"><span data-stu-id="61e89-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="61e89-109">によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="61e89-109">Created by:</span></span>  <br/> |<span data-ttu-id="61e89-110">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="61e89-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="61e89-111">によってアクセスします。</span><span class="sxs-lookup"><span data-stu-id="61e89-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="61e89-112">Outlook およびその他のクライアント</span><span class="sxs-lookup"><span data-stu-id="61e89-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="61e89-113">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="61e89-113">Property type:</span></span>  <br/> |<span data-ttu-id="61e89-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="61e89-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="61e89-115">アクセスの種類:</span><span class="sxs-lookup"><span data-stu-id="61e89-115">Access type:</span></span>  <br/> |<span data-ttu-id="61e89-116">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="61e89-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61e89-117">注釈</span><span class="sxs-lookup"><span data-stu-id="61e89-117">Remarks</span></span>

<span data-ttu-id="61e89-118">ストア機能を提供するストア プロバイダーを実装する必要があります[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) 、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)の呼び出しに渡されたこれらのプロパティのいずれかのプロパティの有効なタグを返すとします。</span><span class="sxs-lookup"><span data-stu-id="61e89-118">To provide any of the store functionality, the store provider must implement [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="61e89-119">これらのプロパティのいずれかのプロパティ タグが[IMAPIProp::GetProps](imapiprop-getprops.md)に渡されると、ストア プロバイダーを使用、正しいプロパティ値を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="61e89-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="61e89-120">ストア プロバイダーには、取得、またはこれらのプロパティを設定するには、 [HrGetOneProp](hrgetoneprop.md)と[HrSetOneProp](hrsetoneprop.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="61e89-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="61e89-121">このプロパティの値を取得するには、クライアントはまず[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を使用して、プロパティ タグを取得して、値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)でこのプロパティのタグを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61e89-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="61e89-122">[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)を呼び出すときは、 _lppPropNames_の入力パラメーターで示される[MAPINAMEID](mapinameid.md)構造体の次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="61e89-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61e89-123">lpGuid。</span><span class="sxs-lookup"><span data-stu-id="61e89-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="61e89-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="61e89-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="61e89-125">ulKind。</span><span class="sxs-lookup"><span data-stu-id="61e89-125">ulKind:</span></span>  <br/> |<span data-ttu-id="61e89-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="61e89-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="61e89-127">Kind.lpwstrName。</span><span class="sxs-lookup"><span data-stu-id="61e89-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="61e89-128">L"urn: スキーマ-マイクロソフト-com:office:outlook #storetypeprivate」</span><span class="sxs-lookup"><span data-stu-id="61e89-128">L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"</span></span>  <br/> |
   
<span data-ttu-id="61e89-129">ストア プロバイダーは、ユーザーのセカンダリ ・ ストアの場合、プライベートとして扱うことがこのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="61e89-129">A store provider can use this property to have Outlook treat it as private when it is a secondary store for a user.</span></span> 
  
<span data-ttu-id="61e89-130">既定では、Outlook として扱われますセカンダリ ・ ストアと同様、代理人のストアで、セカンダリ ・ ストア内の項目のみされた場合は、ユーザーに具体的にはプライベートとしてプライベート。</span><span class="sxs-lookup"><span data-stu-id="61e89-130">By default, Outlook treats a secondary store the same way as a delegate store, and items in the secondary store are private only if the user marks them specifically as private.</span></span> <span data-ttu-id="61e89-131">このプロパティが**true**の場合、セカンダリ ・ ストアから削除されたアイテムは、プライマリ ストアで**削除済みアイテム**フォルダーに移動されます。</span><span class="sxs-lookup"><span data-stu-id="61e89-131">When this property is **true**, items deleted from a secondary store are moved to the **Deleted Items** folder in the primary store.</span></span> <span data-ttu-id="61e89-132">プライベートとしてマークされたアイテムは表示されません。</span><span class="sxs-lookup"><span data-stu-id="61e89-132">Items marked private are not displayed.</span></span> <span data-ttu-id="61e89-133">下書きは、プライマリ ストアで [下書き] フォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="61e89-133">Drafts are stored in the Drafts folder in the primary store.</span></span> 
  
<span data-ttu-id="61e89-134">Outlook のバージョンの Microsoft Office Outlook 2003 Service Pack 1 より前の場合、またはその値が**false**の場合、このプロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="61e89-134">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

