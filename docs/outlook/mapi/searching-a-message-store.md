---
title: メッセージ ストアを検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 90ed7da43d7f9e5e8b5f3024f1eee99a2d7a2b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803848"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="7cee4-103">メッセージ ストアを検索</span><span class="sxs-lookup"><span data-stu-id="7cee4-103">Searching a message store</span></span>

<span data-ttu-id="7cee4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cee4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cee4-105">クライアント アプリケーションは、検索条件に一致するメッセージを探して、1 つまたは複数のフォルダーを検索できます。</span><span class="sxs-lookup"><span data-stu-id="7cee4-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="7cee4-106">最も簡単な検索方法は、抽出条件を定義するのには制限を適用する必要があり、または以前の検索の検索条件に明示的に作成、検索結果フォルダーに結果を配置すること。</span><span class="sxs-lookup"><span data-stu-id="7cee4-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="7cee4-107">すべてのメッセージ ストアは、この手法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="7cee4-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="7cee4-108">決定するかどうか、メッセージ ・ ストアを使用しているをサポートしている検索結果フォルダーを使用して、取得するために[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出す、 **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="7cee4-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="7cee4-109">STORE_SEARCH_OK フラグが設定されている場合に、検索はサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7cee4-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="7cee4-110">設定されていない場合は、ターゲット フォルダーを手動で検査などの別の方法をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7cee4-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="7cee4-111">メッセージ ストアに 1 つまたは複数のフォルダーを検索するには</span><span class="sxs-lookup"><span data-stu-id="7cee4-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="7cee4-112">前の検索から検索結果フォルダーを使っている場合は、手順 2 に進みます。</span><span class="sxs-lookup"><span data-stu-id="7cee4-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="7cee4-113">それ以外の場合、検索結果フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="7cee4-114">検索結果のルート フォルダーのエントリ id を取得するには、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すと、 **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) を要求します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="7cee4-115">PR_FINDER_ENTRYID によって表されるフォルダーを開くには、 [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="7cee4-116">メソッドを呼び出してフォルダーの[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)を FOLDER_SEARCH フラグを設定して、[検索結果] フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="7cee4-117">検索条件を保持するために制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="7cee4-118">検索するフォルダーを表すエントリの識別子の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="7cee4-119">使用されています。 検索結果のフォルダーと同じフォルダーを検索する場合、この手順は必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="7cee4-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="7cee4-120">エントリの識別子の配列を制限する_lpRestriction_ _lpContainerList_を参照、検索結果フォルダーの[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="7cee4-121">メッセージ ・ ストアの検索の完了通知を登録する場合は、到着を通知するため待機します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="7cee4-122">検索結果の内容のテーブルにアクセスするためのフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出すことによって、検索結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="7cee4-123">内容の検索条件を満たすメッセージを取得するテーブルの[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7cee4-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

