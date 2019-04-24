---
title: IMAPIContainer imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer
api_type:
- COM
ms.assetid: d83fdd83-3e86-43c8-a73f-8e9e01b53371
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8be3b1857d539f81e42d2ac3e5813afa73513a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286721"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="ecb6f-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ecb6f-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="ecb6f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecb6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecb6f-105">アドレス帳、配布リスト、フォルダーなどのコンテナーオブジェクトの高レベルの操作を管理します。</span><span class="sxs-lookup"><span data-stu-id="ecb6f-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="ecb6f-106">[imapifolder: IMAPIContainer](imapifolderimapicontainer.md)、 [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)、および[idistlist: IMAPIContainer](idistlistimapicontainer.md)インターフェイスは、 **IMAPIContainer**から派生します。</span><span class="sxs-lookup"><span data-stu-id="ecb6f-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecb6f-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ecb6f-107">Header file:</span></span>  <br/> |<span data-ttu-id="ecb6f-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecb6f-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ecb6f-109">公開者:</span><span class="sxs-lookup"><span data-stu-id="ecb6f-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="ecb6f-110">フォルダー、アドレス帳コンテナー、および配布リストオブジェクト</span><span class="sxs-lookup"><span data-stu-id="ecb6f-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="ecb6f-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="ecb6f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ecb6f-112">メッセージストア、アドレス帳、リモートトランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="ecb6f-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="ecb6f-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ecb6f-113">Called by:</span></span>  <br/> |<span data-ttu-id="ecb6f-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ecb6f-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="ecb6f-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="ecb6f-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ecb6f-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="ecb6f-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="ecb6f-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="ecb6f-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="ecb6f-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="ecb6f-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="ecb6f-119">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="ecb6f-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="ecb6f-120">抽象クラス、実装されていません</span><span class="sxs-lookup"><span data-stu-id="ecb6f-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ecb6f-121">v の順序</span><span class="sxs-lookup"><span data-stu-id="ecb6f-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ecb6f-122">getcontentstable</span><span class="sxs-lookup"><span data-stu-id="ecb6f-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="ecb6f-123">コンテナーの contents テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ecb6f-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="ecb6f-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="ecb6f-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="ecb6f-125">コンテナーの階層テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ecb6f-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="ecb6f-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ecb6f-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="ecb6f-127">コンテナー内のオブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ecb6f-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="ecb6f-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="ecb6f-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="ecb6f-129">コンテナーの検索条件を確立します。</span><span class="sxs-lookup"><span data-stu-id="ecb6f-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="ecb6f-130">getsearchcriteria</span><span class="sxs-lookup"><span data-stu-id="ecb6f-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="ecb6f-131">コンテナーの検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="ecb6f-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="ecb6f-132">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="ecb6f-132">**Required properties**</span></span>|<span data-ttu-id="ecb6f-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="ecb6f-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ecb6f-134">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ecb6f-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ecb6f-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ecb6f-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="ecb6f-136">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ecb6f-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ecb6f-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ecb6f-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="ecb6f-138">**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ecb6f-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ecb6f-139">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ecb6f-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ecb6f-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecb6f-140">See also</span></span>



[<span data-ttu-id="ecb6f-141">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="ecb6f-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

