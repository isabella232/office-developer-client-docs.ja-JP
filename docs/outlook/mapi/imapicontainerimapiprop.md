---
title: IMAPIContainer IMAPIProp
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
ms.openlocfilehash: e24f5ebd73a4652876282099f1460762c150b94d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800455"
---
# <a name="imapicontainer--imapiprop"></a><span data-ttu-id="00625-103">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="00625-103">IMAPIContainer : IMAPIProp</span></span>

  
  
<span data-ttu-id="00625-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00625-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00625-105">アドレス帳、配布リスト、フォルダーなどのコンテナー オブジェクトの高度な処理を管理します。</span><span class="sxs-lookup"><span data-stu-id="00625-105">Manages high-level operations on container objects such as address books, distribution lists, and folders.</span></span> <span data-ttu-id="00625-106">[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)、[これにより: IMAPIContainer](iabcontainerimapicontainer.md)、および[IDistList: IMAPIContainer](idistlistimapicontainer.md)インタ フェースは、 **IMAPIContainer**から派生します。</span><span class="sxs-lookup"><span data-stu-id="00625-106">The [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md), [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md), and [IDistList : IMAPIContainer](idistlistimapicontainer.md) interfaces are derived from **IMAPIContainer**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00625-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="00625-107">Header file:</span></span>  <br/> |<span data-ttu-id="00625-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00625-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="00625-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="00625-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="00625-110">フォルダー、アドレス帳コンテナー、および配布リスト内のオブジェクト</span><span class="sxs-lookup"><span data-stu-id="00625-110">Folder, address book container, and distribution list objects</span></span>  <br/> |
|<span data-ttu-id="00625-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="00625-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="00625-112">メッセージ ・ ストア、アドレス帳、およびリモート トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="00625-112">Message store, address book, and remote transport providers</span></span>  <br/> |
|<span data-ttu-id="00625-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="00625-113">Called by:</span></span>  <br/> |<span data-ttu-id="00625-114">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="00625-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="00625-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="00625-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="00625-116">IID_IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="00625-116">IID_IMAPIContainer</span></span>  <br/> |
|<span data-ttu-id="00625-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="00625-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="00625-118">LPMAPICONTAINER</span><span class="sxs-lookup"><span data-stu-id="00625-118">LPMAPICONTAINER</span></span>  <br/> |
|<span data-ttu-id="00625-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="00625-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="00625-120">抽象クラスで実装されることはありません。</span><span class="sxs-lookup"><span data-stu-id="00625-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="00625-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="00625-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="00625-122">GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="00625-122">GetContentsTable</span></span>](imapicontainer-getcontentstable.md) <br/> |<span data-ttu-id="00625-123">コンテナーの内容のテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="00625-123">Returns a pointer to the container's contents table.</span></span>  <br/> |
|[<span data-ttu-id="00625-124">GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="00625-124">GetHierarchyTable</span></span>](imapicontainer-gethierarchytable.md) <br/> |<span data-ttu-id="00625-125">コンテナーの階層構造のテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="00625-125">Returns a pointer to the container's hierarchy table.</span></span>  <br/> |
|[<span data-ttu-id="00625-126">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="00625-126">OpenEntry</span></span>](imapicontainer-openentry.md) <br/> |<span data-ttu-id="00625-127">コンテナーで、さらにアクセスするためのインターフェイス ポインターを返すには、オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="00625-127">Opens an object in the container, returning an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="00625-128">SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="00625-128">SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md) <br/> |<span data-ttu-id="00625-129">コンテナーの検索基準を確立します。</span><span class="sxs-lookup"><span data-stu-id="00625-129">Establishes search criteria for the container.</span></span>  <br/> |
|[<span data-ttu-id="00625-130">GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="00625-130">GetSearchCriteria</span></span>](imapicontainer-getsearchcriteria.md) <br/> |<span data-ttu-id="00625-131">コンテナーの検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="00625-131">Obtains the search criteria for the container.</span></span>  <br/> |
   
|<span data-ttu-id="00625-132">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="00625-132">**Required properties**</span></span>|<span data-ttu-id="00625-133">**Access**</span><span class="sxs-lookup"><span data-stu-id="00625-133">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00625-134">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="00625-134">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="00625-135">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="00625-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="00625-136">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="00625-136">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="00625-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="00625-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="00625-138">**PR_CONTAINER_FLAGS**([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="00625-138">**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="00625-139">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="00625-139">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00625-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="00625-140">See also</span></span>



[<span data-ttu-id="00625-141">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="00625-141">MAPI Interfaces</span></span>](mapi-interfaces.md)

