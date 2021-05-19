---
title: メッセージ ストアの検証と初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433690"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="ccd54-103">メッセージ ストアの検証と初期化</span><span class="sxs-lookup"><span data-stu-id="ccd54-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="ccd54-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccd54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccd54-105">MDB_NO_MAIL フラグを設定せずに [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) メソッドを使用してメッセージ ストアを開く場合、MAPI は複数のフォルダーを作成し、既定の名前と役割を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ccd54-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="ccd54-106">MAPI は、クライアントまたはメッセージ ストア プロバイダーが作成の責任を負った場合に必然的に発生する非互換性を回避するために、これらのフォルダーを作成する責任があります。</span><span class="sxs-lookup"><span data-stu-id="ccd54-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="ccd54-107">適切なフォルダーが作成され、有効なフォルダーを確認する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="ccd54-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="ccd54-108">[HrValidateIPMSubtree](hrvalidateipmsubtree.md)関数は、この目的のために使用できます。</span><span class="sxs-lookup"><span data-stu-id="ccd54-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="ccd54-109">既定のメッセージ ストアを検証する場合は、既定のメッセージ MAPI_FULL_IPM_TREE渡します。</span><span class="sxs-lookup"><span data-stu-id="ccd54-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="ccd54-110">既定のメッセージ ストア用に、フォルダーのより広範なグループが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ccd54-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="ccd54-111">**HrValidateIPMSubtree** が MAPI_FULL_IPM_TREEフラグを受け取った場合、次のフォルダーがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="ccd54-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="ccd54-112">IPM サブツリーのルート フォルダー</span><span class="sxs-lookup"><span data-stu-id="ccd54-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="ccd54-113">IPM ルート フォルダー内の削除済みアイテム フォルダー</span><span class="sxs-lookup"><span data-stu-id="ccd54-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="ccd54-114">IPM ルート フォルダー内の受信トレイ フォルダー</span><span class="sxs-lookup"><span data-stu-id="ccd54-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="ccd54-115">IPM ルート フォルダー内の送信ボックス フォルダー</span><span class="sxs-lookup"><span data-stu-id="ccd54-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="ccd54-116">IPM ルート フォルダーの [送信されたアイテム] フォルダー</span><span class="sxs-lookup"><span data-stu-id="ccd54-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="ccd54-117">メッセージ ストアのルート フォルダー内のフォルダー ビュー</span><span class="sxs-lookup"><span data-stu-id="ccd54-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="ccd54-118">メッセージ ストアのルート フォルダーの一般的なビュー</span><span class="sxs-lookup"><span data-stu-id="ccd54-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="ccd54-119">メッセージ ストアのルート フォルダー内の検索フォルダー</span><span class="sxs-lookup"><span data-stu-id="ccd54-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="ccd54-120">メッセージ ストアが既定ではない場合は、メッセージ ストア フラグを設定または設定MAPI_FULL_IPM_TREEできます。</span><span class="sxs-lookup"><span data-stu-id="ccd54-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="ccd54-121">このフラグを設定しない場合 **、HrValidateIPMSubtree** は、サブツリーのルート フォルダー、削除済みアイテム フォルダー、およびメッセージ ストア検索結果のルート フォルダーのみをチェックします。</span><span class="sxs-lookup"><span data-stu-id="ccd54-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="ccd54-122">メッセージ ストアを初期化するには、次のプロパティをメモリに格納して、すぐに使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ccd54-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="ccd54-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ccd54-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="ccd54-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ccd54-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="ccd54-125">これらのプロパティは、メッセージ ストアの機能を記述するビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ccd54-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="ccd54-126">**PR_VALID_FOLDER_MASK** ストアに存在する特別なフォルダーごとに 1 ビットが設定され、有効なエントリ識別子が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="ccd54-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="ccd54-127">これらのフォルダーとそのエントリ識別子へのアクセスの詳細については、「メッセージ ストア フォルダーを開 [く」を参照してください](opening-a-message-store-folder.md)。</span><span class="sxs-lookup"><span data-stu-id="ccd54-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="ccd54-128">**PR_STORE_SUPPORT_MASK** ストアでサポートされる機能ごとに 1 ビットが設定されています。</span><span class="sxs-lookup"><span data-stu-id="ccd54-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="ccd54-129">たとえば、メッセージ ストアで通知と書式設定されたテキストがサポートされている場合、メッセージ ストアのPR_STORE_SUPPORT_MASKビットとSTORE_NOTIFY_OKビットSTORE_RTF_OK設定されます。</span><span class="sxs-lookup"><span data-stu-id="ccd54-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="ccd54-130">ローカルに保存する必要があるその他のプロパティには、PR_VALID_FOLDER_MASK **プロパティが** 有効と記述するフォルダーのエントリ識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ccd54-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="ccd54-131">受信トレイ フォルダーを除くこれらの特別なフォルダーのそれぞれには、エントリ識別子プロパティが関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="ccd54-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="ccd54-132">たとえば、Outbox フォルダーのエントリ識別子は、PR_IPM_OUTBOX_ENTRYID **(** [PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="ccd54-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="ccd54-133">これらのフォルダーは頻繁に開くフォルダーなので、エントリ識別子を簡単に使用できるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ccd54-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

