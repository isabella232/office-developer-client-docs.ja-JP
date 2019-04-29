---
title: メッセージストアの検証と初期化
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
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="91c76-103">メッセージストアの検証と初期化</span><span class="sxs-lookup"><span data-stu-id="91c76-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="91c76-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91c76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91c76-105">MDB_NO_MAIL フラグを設定せずに[imapisession:: openmsgstore](imapisession-openmsgstore.md)メソッドを使用してメッセージストアを開くと、MAPI によって複数のフォルダーが作成され、それらに既定の名前と役割が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="91c76-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="91c76-106">MAPI は、クライアントまたはメッセージストアプロバイダーのいずれかが作成を担当した場合に必然的に発生する非互換性を回避するために、これらのフォルダーを作成する責任があります。</span><span class="sxs-lookup"><span data-stu-id="91c76-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="91c76-107">適切なフォルダーが作成され、それらが有効であることを確認する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="91c76-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="91c76-108">このためには、 [hrvalidateipmsubtree](hrvalidateipmsubtree.md)関数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="91c76-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="91c76-109">既定のメッセージストアを検証する場合は、MAPI_FULL_IPM_TREE フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="91c76-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="91c76-110">既定のメッセージストア用に、より広範なフォルダーのグループが作成されます。</span><span class="sxs-lookup"><span data-stu-id="91c76-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="91c76-111">**hrvalidateipmsubtree**が MAPI_FULL_IPM_TREE フラグを受け取ると、次のフォルダーがあるかどうかがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="91c76-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="91c76-112">IPM サブツリーのルートフォルダー</span><span class="sxs-lookup"><span data-stu-id="91c76-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="91c76-113">IPM ルートフォルダーの削除済みアイテムフォルダー</span><span class="sxs-lookup"><span data-stu-id="91c76-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="91c76-114">IPM ルートフォルダーの受信トレイフォルダー</span><span class="sxs-lookup"><span data-stu-id="91c76-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="91c76-115">IPM ルートフォルダーの送信トレイフォルダー</span><span class="sxs-lookup"><span data-stu-id="91c76-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="91c76-116">[送信済みアイテム] フォルダー (IPM ルートフォルダー内)</span><span class="sxs-lookup"><span data-stu-id="91c76-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="91c76-117">メッセージストアのルートフォルダー内のフォルダービュー</span><span class="sxs-lookup"><span data-stu-id="91c76-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="91c76-118">メッセージストアのルートフォルダー内の共通ビュー</span><span class="sxs-lookup"><span data-stu-id="91c76-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="91c76-119">メッセージストアのルートフォルダー内の検索フォルダー</span><span class="sxs-lookup"><span data-stu-id="91c76-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="91c76-120">メッセージストアが既定ではない場合は、MAPI_FULL_IPM_TREE フラグを設定するかどうかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="91c76-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="91c76-121">このフラグが設定されていない場合、 **hrvalidateipmsubtree**はサブツリーのルートフォルダー、削除済みアイテムフォルダー、およびメッセージストア検索結果のルートフォルダーだけをチェックします。</span><span class="sxs-lookup"><span data-stu-id="91c76-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="91c76-122">メッセージストアを初期化するには、次のプロパティをメモリに格納して、簡単に使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="91c76-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="91c76-123">**PR_VALID_FOLDER_MASK**([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="91c76-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="91c76-124">**PR_STORE_SUPPORT_MASK**([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="91c76-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="91c76-125">これらのプロパティは、メッセージストアの機能を記述するビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="91c76-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="91c76-126">**PR_VALID_FOLDER_MASK**には、メッセージストアに存在し、有効なエントリ識別子が割り当てられているすべての特別なフォルダーに対して1ビットが設定されています。</span><span class="sxs-lookup"><span data-stu-id="91c76-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="91c76-127">これらのフォルダーおよびそのエントリ識別子へのアクセスの詳細については、「[メッセージストアフォルダーを開く](opening-a-message-store-folder.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="91c76-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="91c76-128">**PR_STORE_SUPPORT_MASK**には、メッセージストアでサポートされているすべての機能に対して1ビットが設定されています。</span><span class="sxs-lookup"><span data-stu-id="91c76-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="91c76-129">たとえば、メッセージストアが通知と書式設定されたテキストをサポートしている場合、その**PR_STORE_SUPPORT_MASK**には STORE_NOTIFY_OK と STORE_RTF_OK のビットが設定されます。</span><span class="sxs-lookup"><span data-stu-id="91c76-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="91c76-130">ローカルに格納する必要があるその他のプロパティには、 **PR_VALID_FOLDER_MASK**プロパティが有効として記述するフォルダーのエントリ識別子があります。</span><span class="sxs-lookup"><span data-stu-id="91c76-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="91c76-131">受信トレイフォルダー以外の各特別なフォルダーには、エントリ識別子プロパティが関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="91c76-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="91c76-132">たとえば、送信トレイフォルダーのエントリ識別子は、 **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="91c76-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="91c76-133">これらのフォルダーは頻繁に開かれるフォルダーなので、エントリ識別子をすぐに使用できるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="91c76-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

