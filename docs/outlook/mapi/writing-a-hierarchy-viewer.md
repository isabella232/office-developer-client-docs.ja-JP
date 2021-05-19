---
title: 階層ビューアーの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421131"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="e0fb7-103">階層ビューアーの作成</span><span class="sxs-lookup"><span data-stu-id="e0fb7-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="e0fb7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0fb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0fb7-105">階層ビューアーは、フォルダーおよびアドレス帳コンテナー階層テーブルの表示に使用されるユーザー インターフェイス コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="e0fb7-106">階層ビューアーは、階層のメンバーを異なるレベルで表示し、各レベルをオンデマンドで拡張および契約できます。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="e0fb7-107">container プロパティ **(PR_DEPTH** ([PidTagDepth)](pidtagdepth-canonical-property.md)は、階層メンバーが表示されるレベルを制御します。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="e0fb7-108">トップ レベルのアドレス帳コンテナーまたはフォルダーを表すエントリのプロパティPR_DEPTH **0** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="e0fb7-109">このプロパティの値は、順次レベルのエントリに対して順次増分されます。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="e0fb7-110">つまり、ユーザーが展開するトップ レベル のコンテナーを選択すると、すべてのコンテナーが1 に設定PR_DEPTH表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="e0fb7-111">ユーザーがこれらのサブコンテナーの 1 **つ** を展開すると、コンテナーを 2 PR_DEPTHに設定して表示します。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="e0fb7-112">階層ビューアーは、さまざまな範囲の深度をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="e0fb7-113">閲覧者を 1 つまたは 2 つのレベルに制限するか、階層の拡大が優先される場合は複数のレベルをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="e0fb7-114">アドレス帳は、アドレス帳内のトップ レベル コンテナーの階層ビューアーを提供します。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="e0fb7-115">**アドレス帳階層テーブルにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="e0fb7-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="e0fb7-116">[IAddrBook::OpenEntry](iaddrbook-openentry.md)を呼び出し、null エントリ識別子を渡して、アドレス帳のルート コンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="e0fb7-117">MAPI アドレス帳の階層テーブルにアクセスするには、ルート コンテナーの [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="e0fb7-118">**既定のメッセージ ストアの階層テーブルにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="e0fb7-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="e0fb7-119">[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出して、メッセージ ストア テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="e0fb7-120">[SPropertyRestriction](spropertyrestriction.md)構造体を使用して制限を作成し、テーブルを PR_DEFAULT_STORE ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティが **TRUE** に設定されている行にのみ制限します。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="e0fb7-121">[IMAPITable::FindRow](imapitable-findrow.md)を呼び出し **、SPropertyRestriction** を渡して、既定のメッセージ ストアを表す行を探します。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="e0fb7-122">[IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出し **、PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティをメッセージ ストア テーブルの既定のメッセージ ストアの行から渡します。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="e0fb7-123">メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_IPM_SUBTREE_ENTRYID **(** [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="e0fb7-124">メッセージ ストアの [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出し **、PR_IPM_SUBTREE_ENTRYID** プロパティを渡して、メッセージ ストアの IPM サブツリーのルート フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="e0fb7-125">IPM ルート フォルダーの [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出して、その階層テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e0fb7-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

