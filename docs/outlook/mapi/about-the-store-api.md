---
title: ストア API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 31aff61ec5868b0f1e9ab34d498b2e8175519f0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799631"
---
# <a name="about-the-store-api"></a><span data-ttu-id="f97bc-103">ストア API について</span><span class="sxs-lookup"><span data-stu-id="f97bc-103">About the Store API</span></span>

  
  
<span data-ttu-id="f97bc-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f97bc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f97bc-105">保存の API では、プロバイダーを格納するその他のストアの機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="f97bc-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="f97bc-106">次の定義、データ型、プロパティ、およびインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="f97bc-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="f97bc-107">定義</span><span class="sxs-lookup"><span data-stu-id="f97bc-107">Definitions:</span></span>
  
- [<span data-ttu-id="f97bc-108">ストア API の定数</span><span class="sxs-lookup"><span data-stu-id="f97bc-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="f97bc-109">データ型:</span><span class="sxs-lookup"><span data-stu-id="f97bc-109">Data types:</span></span>
  
- <span data-ttu-id="f97bc-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="f97bc-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="f97bc-112">名前付きプロパティ。</span><span class="sxs-lookup"><span data-stu-id="f97bc-112">Named Properties:</span></span>
  
- <span data-ttu-id="f97bc-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="f97bc-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="f97bc-115">**[サーバーのフォルダーのサイズを表示します。](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="f97bc-116">**[会議の更新] オプションを非表示にします。](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="f97bc-117">**[ストアの種類のプライベート](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="f97bc-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="f97bc-119">これらの名前付きプロパティによって提供される機能のいずれかを必要としないストアのプロバイダーでは、単純に無視でき、 **IMAPIProp**インターフェイスのサポートを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="f97bc-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="f97bc-120">これらのプロパティを提供するには、Microsoft Outlook 2003 Service Pack 1 で始まる、ためには、Microsoft Outlook の以前のバージョン ストアに追加することも効果がありません。</span><span class="sxs-lookup"><span data-stu-id="f97bc-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="f97bc-121">存在しない場合、またはその値が**false**の場合、無視されます。</span><span class="sxs-lookup"><span data-stu-id="f97bc-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="f97bc-122">プロパティ:</span><span class="sxs-lookup"><span data-stu-id="f97bc-122">Properties:</span></span>
  
- <span data-ttu-id="f97bc-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="f97bc-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="f97bc-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="f97bc-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="f97bc-127">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f97bc-127">Interfaces:</span></span>
  
- <span data-ttu-id="f97bc-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="f97bc-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="f97bc-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="f97bc-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="f97bc-131">インデックス作成のためのストアを登録します。</span><span class="sxs-lookup"><span data-stu-id="f97bc-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="f97bc-132">MAPI プロトコル ハンドラーでは、検索用のストアにインデックスを作成するための Windows レジストリをチェックします。</span><span class="sxs-lookup"><span data-stu-id="f97bc-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="f97bc-133">インデックスを作成するストア プロバイダーは、Windows レジストリに登録しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f97bc-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="f97bc-134">2013 の Outlook または Outlook 2010 のインデックス作成のためのストア プロバイダーの登録の詳細については、[ストアの登録について](about-registering-stores-for-indexing.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f97bc-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="f97bc-135">ストアのインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f97bc-135">Indexing Stores</span></span>

<span data-ttu-id="f97bc-136">MAPI ストア プロバイダーは、クロールとインデックスのストアにメッセージを MAPI プロトコル ハンドラーを許可するか、インデックスを作成するメッセージがある場合にのみ、インデクサーに対して通知を送信することできます。</span><span class="sxs-lookup"><span data-stu-id="f97bc-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="f97bc-137">通知に基づくインデックス作成の詳細については、 [About Notification-Based ストアのインデックス作成](about-notification-based-store-indexing.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f97bc-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

