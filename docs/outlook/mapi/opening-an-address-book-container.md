---
title: アドレス帳のコンテナーを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436742"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="0fbd3-103">アドレス帳のコンテナーを開く</span><span class="sxs-lookup"><span data-stu-id="0fbd3-103">Opening an address book container</span></span>

<span data-ttu-id="0fbd3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fbd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fbd3-105">MAPI 統合アドレス帳を開いた後、1 つ以上のアドレス帳コンテナーを開いて、その中の受信者にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="0fbd3-106">アドレス帳のトップ レベル コンテナーを開く場合は、NULL エントリ識別子を使用して [IAddrBook::OpenEntry](iaddrbook-openentry.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="0fbd3-107">アドレス帳コンテナーは、読み取り専用または読み取り/書き込みアクセスで実装できます。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="0fbd3-108">読み取り専用コンテナーは、参照にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="0fbd3-109">読み取り/書き込みコンテナーは変更でき、クライアントは新しいエントリを作成し、既存のエントリを削除および変更できます。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="0fbd3-110">すべての個人用アドレス帳 (PAB) コンテナーは、読み取り/書き込みコンテナーとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="0fbd3-111">下位レベルのコンテナーを開く場合は **、OpenEntry** を呼び出し、開くコンテナーのエントリ識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="0fbd3-112">PAB として指定されているコンテナーを開く</span><span class="sxs-lookup"><span data-stu-id="0fbd3-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="0fbd3-113">[IAddrBook::GetPAB](iaddrbook-getpab.md)を呼び出して、PAB のエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="0fbd3-114">このエントリ識別子を [IAddrBook::OpenEntry に渡します](iaddrbook-openentry.md)。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="0fbd3-115">PAB ではないコンテナーを開く</span><span class="sxs-lookup"><span data-stu-id="0fbd3-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="0fbd3-116">アドレス帳のルート コンテナーを開く NULL エントリ識別子を使用して [IAddrBook::OpenEntry](iaddrbook-openentry.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="0fbd3-117">ルート コンテナーの [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) メソッドを呼び出して、その階層テーブル (アドレス帳内のすべてのトップ レベル コンテナーのリスト) を取得します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="0fbd3-118">開くコンテナーが特定の種類の場合:</span><span class="sxs-lookup"><span data-stu-id="0fbd3-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="0fbd3-119">プロパティ タグの **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))、プロパティ値のコンテナーの型、およびリレーションの RELOP_EQ を持つ **SPropertyRestriction** 構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="0fbd3-120">**PR_DISPLAY_TYPE** は、次の中で多数の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="0fbd3-121">DT_GLOBAL、階層テーブルをグローバル アドレス一覧に属するコンテナーに制限します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="0fbd3-122">DT_LOCALアドレス帳に属するコンテナーにテーブルを制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="0fbd3-123">DT_MODIFIABLE変更可能なコンテナーにテーブルを制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="0fbd3-124">[SPropTagArray](sproptagarray.md)構造体を作成し **、PR_ENTRYID、PR_DISPLAY_TYPE** その **他** の列を含む構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="0fbd3-125">[HrQueryAllRows を呼び](hrqueryallrows.md)出し、プロパティ制限とプロパティ タグ配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="0fbd3-126">**HrQueryAllRows は** 、指定した型に属するコンテナーごとに 0 行以上の行を返します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="0fbd3-127">任意の数の行の戻り値を処理する準備をしてください。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="0fbd3-128">**IAddrBook::OpenEntry** を呼び出し **、** 関心のあるコンテナーを表す行の PR_ENTRYID 列のエントリ識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="0fbd3-129">開くコンテナーが特定のアドレス帳プロバイダーに属している場合:</span><span class="sxs-lookup"><span data-stu-id="0fbd3-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="0fbd3-130">プロパティ タグの **PR_AB_PROVIDERS** ([PidTagAbProviders)、](pidtagabproviders-canonical-property.md)プロパティ値のプロバイダー固有の値、およびリレーションの RELOP_EQ を持つ [SPropertyRestriction](spropertyrestriction.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="0fbd3-131">通常、プロバイダー固有の値は、グローバルに一意の識別子または GUID です。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="0fbd3-132">この値は、アドレス帳プロバイダーのヘッダー ファイルの 1 つで公開されています。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="0fbd3-133">[SPropTagArray](sproptagarray.md)構造体を作成 **し**、PR_ENTRYID ([PidTagEntryId)](pidtagentryid-canonical-property.md)、PR_AB_PROVIDERS、その **他** の関心のある列を含む構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="0fbd3-134">[HrQueryAllRows を呼び](hrqueryallrows.md)出し、プロパティ制限とプロパティ タグ配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="0fbd3-135">指定したアドレス帳プロバイダーがプロファイルに含めされていない場合 **、HrQueryAllRows** は 0 行を返します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="0fbd3-136">プロバイダーの整理方法に応じて、プロバイダーのトップ レベル コンテナーに対して 1 つ以上の行を返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="0fbd3-137">[IAddrBook::OpenEntry](iaddrbook-openentry.md)を呼び出し **、** 関心のあるコンテナーを表す行の PR_ENTRYID 列のエントリ識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="0fbd3-138">関心のあるコンテナーがトップ レベル のコンテナーではない場合は、トップ レベルのコンテナーを見つけて、階層を走査します。</span><span class="sxs-lookup"><span data-stu-id="0fbd3-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

