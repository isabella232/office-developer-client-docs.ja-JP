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
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="e9317-103">階層ビューアーの作成</span><span class="sxs-lookup"><span data-stu-id="e9317-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="e9317-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9317-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9317-105">階層ビューアーは、フォルダーとアドレス帳のコンテナー階層テーブルを表示するために使用されるユーザーインターフェイスコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="e9317-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="e9317-106">階層の閲覧者は、さまざまなレベルで階層のメンバーを表示したり、必要に応じて各レベルを拡張して縮小したりできます。</span><span class="sxs-lookup"><span data-stu-id="e9317-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="e9317-107">container プロパティ**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) は、階層のメンバーが表示されるレベルを制御します。</span><span class="sxs-lookup"><span data-stu-id="e9317-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="e9317-108">トップレベルのアドレス帳のコンテナーまたはフォルダーを表すエントリは、 **PR_DEPTH**プロパティが0に設定されています。</span><span class="sxs-lookup"><span data-stu-id="e9317-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="e9317-109">このプロパティの値は、シーケンシャルレベルのエントリに対して順次インクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="e9317-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="e9317-110">つまり、ユーザーが最上位のコンテナーを選択して展開するときに、 **PR_DEPTH**が1に設定されているすべてのコンテナーを表示します。</span><span class="sxs-lookup"><span data-stu-id="e9317-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="e9317-111">ユーザーがこれらのサブコンテナーの1つを展開すると、 **PR_DEPTH**が2に設定されているコンテナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e9317-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="e9317-112">階層ビューアーでは、異なる深さの範囲がサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e9317-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="e9317-113">ビューアーを1つまたは2つのレベルのみに制限することも、複数のレベルをサポートすることもできます。拡張性の高い階層を表示する場合は、優先度を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e9317-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="e9317-114">アドレス帳には、アドレス帳の最上位のコンテナーの階層ビューアーがあります。</span><span class="sxs-lookup"><span data-stu-id="e9317-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="e9317-115">**アドレス帳階層テーブルにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="e9317-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="e9317-116">[IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出し、null エントリ識別子を渡して、アドレス帳のルートコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e9317-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="e9317-117">ルートコンテナーの[IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、MAPI アドレス帳の階層テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e9317-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="e9317-118">**既定のメッセージストアの階層テーブルにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="e9317-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="e9317-119">呼び出し[imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)メッセージストアテーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e9317-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="e9317-120">[spropertyrestriction](spropertyrestriction.md)構造を使用して制限を構築し、 **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) プロパティが TRUE に設定されている行だけにテーブルを制限します。</span><span class="sxs-lookup"><span data-stu-id="e9317-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="e9317-121">[IMAPITable:: FindRow](imapitable-findrow.md)を呼び出し、 **spropertyrestriction**を渡して、既定のメッセージストアを表す行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="e9317-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="e9317-122">メッセージストアテーブルの既定のメッセージストアの行から**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを渡して、 [imapisession:: openentry](imapisession-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9317-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="e9317-123">メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="e9317-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="e9317-124">メッセージストアの[IMsgStore:: openentry](imsgstore-openentry.md)メソッドを呼び出して、 **PR_IPM_SUBTREE_ENTRYID**プロパティを渡し、メッセージストアの IPM サブツリーのルートフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e9317-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="e9317-125">IPM ルートフォルダーの[IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、その階層テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e9317-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

