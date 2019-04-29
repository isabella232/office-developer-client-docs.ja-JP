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
# <a name="searching-a-message-store"></a><span data-ttu-id="47a9a-103">メッセージ ストアの検索</span><span class="sxs-lookup"><span data-stu-id="47a9a-103">Searching a message store</span></span>

<span data-ttu-id="47a9a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47a9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47a9a-105">クライアントアプリケーションは、検索条件に一致するメッセージを検索するために、1つまたは複数のフォルダーを検索できます。</span><span class="sxs-lookup"><span data-stu-id="47a9a-105">Client applications can search through one or more folders looking for messages that match search criteria.</span></span> <span data-ttu-id="47a9a-106">最も単純な検索手法では、条件を定義し、その結果を検索結果フォルダーに格納する制限を適用して、この検索または以前の検索に対して明示的に作成します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-106">The most straightforward search technique involves applying a restriction to define criteria and placing the results into a search-results folder, created explicitly for this search or for a prior search.</span></span> <span data-ttu-id="47a9a-107">すべてのメッセージストアがこの手法をサポートするわけではありません。</span><span class="sxs-lookup"><span data-stu-id="47a9a-107">Not all message stores support this technique.</span></span> 

<span data-ttu-id="47a9a-108">使用しているメッセージストアが検索結果フォルダーの使用をサポートしているかどうかを判断するには、 **\_PR STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを取得するのには、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-108">To determine whether or not the message store you are using supports using search-results folders, call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="47a9a-109">STORE_SEARCH_OK フラグが設定されている場合は、検索がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="47a9a-109">If the STORE_SEARCH_OK flag is set, searching is supported.</span></span> <span data-ttu-id="47a9a-110">設定されていない場合は、ターゲットフォルダーを手動で検査するなどの別の方法が必要になります。</span><span class="sxs-lookup"><span data-stu-id="47a9a-110">If it is not set, you'll need an alternate approach such as manually inspecting the target folders.</span></span>
  
### <a name="to-search-one-or-more-folders-in-a-message-store"></a><span data-ttu-id="47a9a-111">メッセージストア内の1つまたは複数のフォルダーを検索するには</span><span class="sxs-lookup"><span data-stu-id="47a9a-111">To search one or more folders in a message store</span></span>
  
1. <span data-ttu-id="47a9a-112">以前の検索からの検索結果フォルダーがある場合は、手順2に進みます。</span><span class="sxs-lookup"><span data-stu-id="47a9a-112">If you have a search-results folder from a previous search, skip to step 2.</span></span> <span data-ttu-id="47a9a-113">それ以外の場合は、検索結果フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-113">Otherwise, to create a search-results folder:</span></span>
    
    1. <span data-ttu-id="47a9a-114">メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) を要求することにより、検索結果のルートフォルダーのエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-114">Retrieve the entry identifier for the search-results root folder by calling the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method and requesting **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="47a9a-115">[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、PR_FINDER_ENTRYID によって表されるフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="47a9a-115">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the folder represented by PR_FINDER_ENTRYID.</span></span> 
        
    3. <span data-ttu-id="47a9a-116">フォルダーの[imapifolder:: CreateFolder](imapifolder-createfolder.md)メソッドを呼び出して、FOLDER_SEARCH フラグが設定された検索結果フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-116">Call the folder's [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method to create a search-results folder with the FOLDER_SEARCH flag set.</span></span> 
    
2. <span data-ttu-id="47a9a-117">検索条件を保持する制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-117">Build a restriction to hold your search criteria.</span></span> 
    
3. <span data-ttu-id="47a9a-118">検索するフォルダーを表すエントリ識別子の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-118">Create an array of entry identifiers that represent the folders to search.</span></span> <span data-ttu-id="47a9a-119">検索結果フォルダーが以前に使用されていて、同じフォルダーを検索する場合は、この手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="47a9a-119">This step is unnecessary if the search-results folder has been used before and you want to search the same folders.</span></span>
    
4. <span data-ttu-id="47a9a-120">検索結果フォルダーの[IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドを呼び出し、 _lpContainerList_をエントリ識別子の配列に、lpRestriction を制限に__ します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-120">Call the search-results folder's [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method, pointing  _lpContainerList_ to the entry identifier array and  _lpRestriction_ to the restriction.</span></span> 
    
5. <span data-ttu-id="47a9a-121">メッセージストアで検索完了通知を登録している場合は、通知が到着するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-121">If you have registered for search complete notifications with the message store, wait for the notification to arrive.</span></span>
    
6. <span data-ttu-id="47a9a-122">検索結果フォルダーの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出して、そのコンテンツテーブルにアクセスし、検索結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-122">View the results of the search by calling the search-results folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access its contents table.</span></span> 
    
7. <span data-ttu-id="47a9a-123">コンテンツテーブルの[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出して、検索条件に一致するメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="47a9a-123">Call the contents table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the messages that satisfy the search criteria.</span></span> 
    

