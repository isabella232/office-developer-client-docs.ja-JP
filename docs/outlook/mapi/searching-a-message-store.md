---
title: メッセージ ストアの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9e8d4639-7507-4d98-b56f-a65be369dc40
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7240f49a15fdaea4d1f30dae578d25c3f2c1c0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426038"
---
# <a name="searching-a-message-store"></a><span data-ttu-id="97cb5-103">メッセージ ストアの検索</span><span class="sxs-lookup"><span data-stu-id="97cb5-103">Searching a message store</span></span>

<span data-ttu-id="97cb5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97cb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97cb5-105">クライアント アプリケーションは、検索条件に一致するメッセージを検索する 1 つ以上のフォルダーを検索できます。</span><span class="sxs-lookup"><span data-stu-id="97cb5-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="97cb5-106">最も簡単な検索方法は、条件を定義する制限を適用し、この検索または以前の検索用に明示的に作成された検索結果フォルダーに結果を配置する方法です。</span><span class="sxs-lookup"><span data-stu-id="97cb5-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="97cb5-107">一部のメッセージ ストアでは、この手法がサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="97cb5-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="97cb5-108">使用しているメッセージ ストアが検索結果フォルダーの使用をサポートするかどうかを確認するには [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="97cb5-109">このフラグSTORE_SEARCH_OK設定されている場合は、検索がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="97cb5-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="97cb5-110">設定されていない場合は、ターゲット フォルダーを手動で検査するなどの別の方法が必要です。</span><span class="sxs-lookup"><span data-stu-id="97cb5-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="97cb5-111">メッセージ ストア内の 1 つ以上のフォルダーを検索するには</span><span class="sxs-lookup"><span data-stu-id="97cb5-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="97cb5-112">以前の検索から検索結果フォルダーがある場合は、手順 2 に進みます。</span><span class="sxs-lookup"><span data-stu-id="97cb5-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="97cb5-113">それ以外の場合は、検索結果フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="97cb5-114">メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出し、PR_FINDER_ENTRYID ([PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)を要求して、検索結果 **ルート** フォルダーのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="97cb5-115">[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出して、ユーザーが表すフォルダーを開PR_FINDER_ENTRYID。</span><span class="sxs-lookup"><span data-stu-id="97cb5-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="97cb5-116">フォルダーの [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) メソッドを呼び出して、検索結果フォルダーを作成し、FOLDER_SEARCH設定します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="97cb5-117">検索条件を保持するための制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="97cb5-118">検索するフォルダーを表すエントリ識別子の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="97cb5-119">検索結果フォルダーが以前に使用され、同じフォルダーを検索する場合は、この手順は不要です。</span><span class="sxs-lookup"><span data-stu-id="97cb5-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="97cb5-120">検索結果フォルダーの [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) メソッドを呼び出し  _、lpContainerList_ をエントリ識別子配列に  _、lpRestriction_ を制限に指定します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="97cb5-121">メッセージ ストアで検索完了通知を登録している場合は、通知が届くのを待ちます。</span><span class="sxs-lookup"><span data-stu-id="97cb5-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="97cb5-122">検索結果フォルダーの [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) メソッドを呼び出して、そのコンテンツ テーブルにアクセスして、検索の結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="97cb5-123">コンテンツ テーブルの [IMAPITable::QueryRows](imapitable-queryrows.md) メソッドを呼び出して、検索条件を満たすメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="97cb5-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

