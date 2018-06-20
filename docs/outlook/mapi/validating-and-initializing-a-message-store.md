---
title: 検証して、メッセージ ストアを初期化しています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 48883ec33db9ffd6b3e7cc6e16ae9c2487a31607
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804224"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="d39e5-103">検証して、メッセージ ストアを初期化しています。</span><span class="sxs-lookup"><span data-stu-id="d39e5-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="d39e5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d39e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d39e5-105">MDB_NO_MAIL フラグを設定せずには、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドで、メッセージ ストアを開く、MAPI はいくつかのフォルダーを作成し、それらに既定の名前とロールを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d39e5-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="d39e5-106">MAPI は、クライアントまたはメッセージ ストア プロバイダーの作成を担当する場合としない発生する必然的に非互換性を避けるためにこれらのフォルダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d39e5-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="d39e5-107">適切なフォルダーが作成されていると、有効であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d39e5-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="d39e5-108">[HrValidateIPMSubtree](hrvalidateipmsubtree.md)関数は、この目的のために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d39e5-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="d39e5-109">既定のメッセージ ストアを検査する場合は、MAPI_FULL_IPM_TREE フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="d39e5-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="d39e5-110">フォルダーのより広範なグループは、既定のメッセージ ストアに作成されます。</span><span class="sxs-lookup"><span data-stu-id="d39e5-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="d39e5-111">**HrValidateIPMSubtree**は、MAPI_FULL_IPM_TREE フラグを受信すると、次のフォルダーをチェックします。</span><span class="sxs-lookup"><span data-stu-id="d39e5-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="d39e5-112">IPM サブツリーのルート フォルダー</span><span class="sxs-lookup"><span data-stu-id="d39e5-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="d39e5-113">IPM のルート フォルダー内の削除済みアイテム フォルダー</span><span class="sxs-lookup"><span data-stu-id="d39e5-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d39e5-114">IPM ルート フォルダー内の [受信トレイ] フォルダー</span><span class="sxs-lookup"><span data-stu-id="d39e5-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d39e5-115">IPM のルート フォルダー内のフォルダーを [送信トレイ] します。</span><span class="sxs-lookup"><span data-stu-id="d39e5-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d39e5-116">IPM のルート フォルダー内のアイテム] フォルダーの送信</span><span class="sxs-lookup"><span data-stu-id="d39e5-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="d39e5-117">メッセージ ストアのルート フォルダーにフォルダーの表示</span><span class="sxs-lookup"><span data-stu-id="d39e5-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="d39e5-118">メッセージ ストアのルート フォルダー内の共通のビュー</span><span class="sxs-lookup"><span data-stu-id="d39e5-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="d39e5-119">メッセージ ストアのルート フォルダーにフォルダーを検索</span><span class="sxs-lookup"><span data-stu-id="d39e5-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="d39e5-120">メッセージ ・ ストアが既定値でない場合は、設定か、MAPI_FULL_IPM_TREE フラグが設定されていません。</span><span class="sxs-lookup"><span data-stu-id="d39e5-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="d39e5-121">このフラグが設定されていない場合、 **HrValidateIPMSubtree**が、サブツリーのルート フォルダーだけをチェック、削除済みアイテム フォルダー、およびメッセージのルート フォルダーは、検索結果を格納します。</span><span class="sxs-lookup"><span data-stu-id="d39e5-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="d39e5-122">メッセージ ストアを初期化するためにすぐに利用できるように、次のプロパティをメモリに格納します。</span><span class="sxs-lookup"><span data-stu-id="d39e5-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="d39e5-123">**PR_VALID_FOLDER_MASK**([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d39e5-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="d39e5-124">**PR_STORE_SUPPORT_MASK**([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d39e5-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="d39e5-125">これらのプロパティは、メッセージ ・ ストアの機能を記述するビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d39e5-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="d39e5-126">**PR_VALID_FOLDER_MASK**では、1 ビットがメッセージ ・ ストアに存在し、有効なエントリが割り当てられている識別子を持つすべての特別なフォルダーの設定があります。</span><span class="sxs-lookup"><span data-stu-id="d39e5-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="d39e5-127">これらのフォルダーおよびそれらのエントリの識別子へのアクセスの詳細については、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d39e5-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="d39e5-128">**PR_STORE_SUPPORT_MASK**では、1 ビットがメッセージ ・ ストアでサポートされているすべての機能の設定があります。</span><span class="sxs-lookup"><span data-stu-id="d39e5-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="d39e5-129">たとえば、メッセージ ・ ストアでは、通知、および書式設定されたテキストをサポートする場合、 **PR_STORE_SUPPORT_MASK**は、STORE_NOTIFY_OK と STORE_RTF_OK のビットを設定があります。</span><span class="sxs-lookup"><span data-stu-id="d39e5-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="d39e5-130">ローカルに格納する必要があるその他のプロパティには、 **PR_VALID_FOLDER_MASK**プロパティを有効なものとして説明するフォルダーのエントリ id が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d39e5-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="d39e5-131">受信トレイ] フォルダー以外のこれらの特別なフォルダーには、それに関連するエントリの識別子プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="d39e5-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="d39e5-132">たとえば、[送信トレイ] フォルダーのエントリ id は、その**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="d39e5-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="d39e5-133">これらのフォルダーが頻繁に開かれるフォルダーであるためが、エントリ id をすぐに利用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d39e5-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

