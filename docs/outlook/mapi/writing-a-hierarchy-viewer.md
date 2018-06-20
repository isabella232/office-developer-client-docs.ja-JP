---
title: 階層ビューアーを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0286696707d268867a5536ef345d0af7909918dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804241"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="e1d9e-103">階層ビューアーを作成します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="e1d9e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1d9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1d9e-105">階層ビューアーは、フォルダーとアドレス帳コンテナーの階層テーブルを表示するために使用されるユーザー インターフェイス コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="e1d9e-106">階層ビューアーでは、さまざまなレベル、オン ・ デマンドでの各レベルを変更することで、階層のメンバーを表示できます。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="e1d9e-107">コンテナーのプロパティ、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) は、階層のメンバーを表示するレベルを制御します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="e1d9e-108">最上位のアドレス帳コンテナーまたはフォルダーを表すエントリがある、 **PR_DEPTH**プロパティを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="e1d9e-109">このプロパティの値は連続したレベルにあるエントリを順に増加します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="e1d9e-110">ユーザーが最上位のコンテナーを展開し、表示するを選択すると**PR_DEPTH**を持つすべてのコンテナーは 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="e1d9e-111">ユーザーには、これらのサブコンテナーのいずれかが拡張されと 2、 **PR_DEPTH**のセットを使用してコンテナーを表示するように。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="e1d9e-112">階層ビューアーでは、深さの別の範囲をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="e1d9e-113">ビューアーに 1 つまたは 2 つのレベルを制限することや、複数のレベルをサポートするには、優先度、拡張性のある階層を表示する場合。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="e1d9e-114">アドレス帳には、アドレス帳内の最上位のコンテナーの階層ビューアーが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="e1d9e-115">**アドレス帳の階層テーブルにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="e1d9e-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="e1d9e-116">[アドレス帳コンテナー](iaddrbook-openentry.md)を null のエントリの識別子を渡すことを開くには、アドレス帳のルート コンテナーを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="e1d9e-117">MAPI アドレス帳の階層テーブルにアクセスするためのルート コンテナーの[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="e1d9e-118">**既定のメッセージ ストアの階層テーブルにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="e1d9e-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="e1d9e-119">メッセージ ストアにアクセスする[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="e1d9e-120">[SPropertyRestriction](spropertyrestriction.md)構造体を使用して**PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティが TRUE に設定を持つ行のみのテーブルを制限する制約を作成します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="e1d9e-121">[IMAPITable::FindRow](imapitable-findrow.md)を渡すことを**SPropertyRestriction**既定のメッセージ ストアを表す行を検索するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="e1d9e-122">[IMAPISession::OpenEntry](imapisession-openentry.md)既定のメッセージ ストアのテーブルの行のメッセージ ストアから**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティに渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="e1d9e-123">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) のプロパティを取得するために、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="e1d9e-124">メッセージ ストアの IPM サブツリーのルート フォルダーを開く、 **PR_IPM_SUBTREE_ENTRYID**プロパティを渡すメッセージ ストアの[IMsgStore::OpenEntry](imsgstore-openentry.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="e1d9e-125">階層テーブルにアクセスするための IPM のルート フォルダーの[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d9e-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

