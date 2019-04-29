---
title: ストア API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405556"
---
# <a name="about-the-store-api"></a><span data-ttu-id="4d573-103">ストア API について</span><span class="sxs-lookup"><span data-stu-id="4d573-103">About the Store API</span></span>

  
  
<span data-ttu-id="4d573-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d573-105">store API は、ストアプロバイダーにさまざまなストア機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d573-105">The Store API provides miscellaneous store functionality to store providers.</span></span> <span data-ttu-id="4d573-106">これにより、次の日、データ型、プロパティ、およびインターフェイスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="4d573-106">It provides the following defintions, data types, properties, and interfaces.</span></span>
  
<span data-ttu-id="4d573-107">定義</span><span class="sxs-lookup"><span data-stu-id="4d573-107">Definitions:</span></span>
  
- [<span data-ttu-id="4d573-108">Store API の定数</span><span class="sxs-lookup"><span data-stu-id="4d573-108">Constants for the Store API</span></span>](mapi-constants.md)
    
<span data-ttu-id="4d573-109">データ型:</span><span class="sxs-lookup"><span data-stu-id="4d573-109">Data types:</span></span>
  
- <span data-ttu-id="4d573-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-110">**[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**</span></span>
    
- <span data-ttu-id="4d573-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-111">**[MSCAP_SELECTOR](mscap_selector.md)**</span></span>
    
<span data-ttu-id="4d573-112">名前付きプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4d573-112">Named Properties:</span></span>
  
- <span data-ttu-id="4d573-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-113">**[ArchiveSourceSupportMask](archivesourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="4d573-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-114">**[CrawlSourceSupportMask](crawlsourcesupportmask.md)**</span></span>
    
- <span data-ttu-id="4d573-115">**[サーバーフォルダーのサイズを表示する](display-server-folder-sizes-property.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-115">**[Display Server Folder Sizes](display-server-folder-sizes-property.md)**</span></span>
    
- <span data-ttu-id="4d573-116">**[会議の更新オプションを非表示にする](hide-meeting-update-option-property.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-116">**[Hide Meeting Update Option](hide-meeting-update-option-property.md)**</span></span>
    
- <span data-ttu-id="4d573-117">**[ストアの種類をプライベートにする](make-store-type-private-property.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-117">**[Make Store Type Private](make-store-type-private-property.md)**</span></span>
    
- <span data-ttu-id="4d573-118">**[NoFolderScan](nofolderscan.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-118">**[NoFolderScan](nofolderscan.md)**</span></span>
    
> [!NOTE]
> <span data-ttu-id="4d573-119">これらの名前付きプロパティによって提供される機能を必要としないストアプロバイダーは、単にそれらを無視して、 **imapiprop**インターフェイスでサポートを実装することはできません。</span><span class="sxs-lookup"><span data-stu-id="4d573-119">Store providers that do not require any of the functionality offered by these named properties can simply ignore them and not implement support in the **IMAPIProp** interface.</span></span> <span data-ttu-id="4d573-120">これらのプロパティは、microsoft outlook 2003 Service Pack 1 以降で提供されるため、以前のバージョンの microsoft outlook でストアに追加しても効果はありません。</span><span class="sxs-lookup"><span data-stu-id="4d573-120">Because these properties are provided starting in Microsoft Outlook 2003 Service Pack 1, adding them to a store in an earlier version of Microsoft Outlook has no effect.</span></span> <span data-ttu-id="4d573-121">存在しない場合、または値が**false**の場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="4d573-121">They are ignored if they do not exist or if their value is **false**.</span></span> 
  
<span data-ttu-id="4d573-122">プロパティ:</span><span class="sxs-lookup"><span data-stu-id="4d573-122">Properties:</span></span>
  
- <span data-ttu-id="4d573-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-123">**[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**</span></span>
    
- <span data-ttu-id="4d573-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-124">**[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="4d573-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-125">**[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**</span></span>
    
- <span data-ttu-id="4d573-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-126">**[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**</span></span>
    
<span data-ttu-id="4d573-127">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="4d573-127">Interfaces:</span></span>
  
- <span data-ttu-id="4d573-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-128">**[IFolderSupport](ifoldersupportiunknown.md)**</span></span>
    
- <span data-ttu-id="4d573-129">**[imscapabilities](imscapabilitiesiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-129">**[IMSCapabilities](imscapabilitiesiunknown.md)**</span></span>
    
- <span data-ttu-id="4d573-130">**[IProxyStoreObject](iproxystoreobject.md)**</span><span class="sxs-lookup"><span data-stu-id="4d573-130">**[IProxyStoreObject](iproxystoreobject.md)**</span></span>
    
## <a name="registering-stores-for-indexing"></a><span data-ttu-id="4d573-131">インデックス作成のためのストアの登録</span><span class="sxs-lookup"><span data-stu-id="4d573-131">Registering Stores for Indexing</span></span>

<span data-ttu-id="4d573-132">MAPI プロトコルハンドラーは、検索用にインデックスが必要なストアの Windows レジストリをチェックします。</span><span class="sxs-lookup"><span data-stu-id="4d573-132">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="4d573-133">インデックスを作成するストアプロバイダーは、Windows レジストリに登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d573-133">Store providers that want to be indexed must be registered in the Windows registry.</span></span> <span data-ttu-id="4d573-134">outlook 2013 または outlook 2010 でのインデックス作成のためのストアプロバイダーの登録の詳細については、「[インデックス作成のためのストア登録につい](about-registering-stores-for-indexing.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d573-134">For more information about registering store providers for indexing in Outlook 2013 or Outlook 2010, see [About Registering Stores for Indexing](about-registering-stores-for-indexing.md).</span></span>
  
## <a name="indexing-stores"></a><span data-ttu-id="4d573-135">インデックス作成ストア</span><span class="sxs-lookup"><span data-stu-id="4d573-135">Indexing Stores</span></span>

<span data-ttu-id="4d573-136">mapi ストアプロバイダーでは、mapi プロトコルハンドラーでストア内のメッセージのクロールとインデックス作成を行うことができます。また、インデックスを作成するメッセージがある場合にのみ、インデクサーに通知を送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="4d573-136">MAPI store providers can choose to allow the MAPI Protocol Handler to crawl and index messages in the store, or send notifications to the indexer only when there are messages to be indexed.</span></span> <span data-ttu-id="4d573-137">通知ベースのインデックス作成の詳細については、「[通知ベースのストアインデックス作成につい](about-notification-based-store-indexing.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d573-137">For more information about notifications-based indexing, see [About Notification-Based Store Indexing](about-notification-based-store-indexing.md).</span></span>
  

