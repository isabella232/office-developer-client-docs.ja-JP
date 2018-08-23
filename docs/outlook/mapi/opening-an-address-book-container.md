---
title: アドレス帳コンテナーを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 28f60154524065bd2c818e2e4b7db37ca33276b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801690"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="89ed2-103">アドレス帳コンテナーを開く</span><span class="sxs-lookup"><span data-stu-id="89ed2-103">Opening an address book container</span></span>

<span data-ttu-id="89ed2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89ed2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89ed2-105">MAPI を開くには、アドレス帳が統合されて後、は、1 つまたは複数のアドレス帳コンテナー内の受信者にアクセスを開きます。</span><span class="sxs-lookup"><span data-stu-id="89ed2-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="89ed2-106">アドレス帳の最上位のコンテナーを開くには、NULL のエントリの識別子を使用して[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="89ed2-107">読み取り専用のアドレス帳コンテナーを実装することができますまたは読み取り/書き込みアクセス。</span><span class="sxs-lookup"><span data-stu-id="89ed2-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="89ed2-108">読み取り専用コンテナーは、参照用にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="89ed2-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="89ed2-109">クライアントが新しいエントリを作成、削除および既存のエントリを変更できるように、読み取り/書き込みのコンテナーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="89ed2-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="89ed2-110">個人用アドレス帳 (PAB) のすべてのコンテナーは、コンテナーの読み取り/書き込みとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="89ed2-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="89ed2-111">より低いレベルのコンテナーを開くには、 **OpenEntry**を呼び出すし、開かれるコンテナーのエントリの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="89ed2-112">個人アドレス帳として指定されているコンテナーを開く</span><span class="sxs-lookup"><span data-stu-id="89ed2-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="89ed2-113">個人用アドレス帳のエントリの識別子を取得する[られたユーザーのプライマリ](iaddrbook-getpab.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="89ed2-114">[アドレス帳コンテナー](iaddrbook-openentry.md)には、このエントリの識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="89ed2-115">個人アドレス帳ではないコンテナーを開く</span><span class="sxs-lookup"><span data-stu-id="89ed2-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="89ed2-116">開くには、アドレス帳のルート コンテナーの NULL エントリ識別子を使用して[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="89ed2-117">階層テーブルを取得するのには、ルート コンテナーの[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、アドレス帳内の最上位のコンテナーのすべてのリスト。</span><span class="sxs-lookup"><span data-stu-id="89ed2-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="89ed2-118">場合は、コンテナーを開くには、特定の種類のです。</span><span class="sxs-lookup"><span data-stu-id="89ed2-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="89ed2-119">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) を持つプロパティ タグは、コンテナーの値の型、プロパティ、関係の RELOP_EQ の**SPropertyRestriction**構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="89ed2-120">**PR_DISPLAY_TYPE**は、それらの間、多くの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="89ed2-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="89ed2-121">グローバル アドレス一覧に属しているコンテナーの階層テーブルを制限する DT_GLOBAL です。</span><span class="sxs-lookup"><span data-stu-id="89ed2-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="89ed2-122">コンテナーがローカルのアドレス帳に所属するテーブルを制限する DT_LOCAL です。</span><span class="sxs-lookup"><span data-stu-id="89ed2-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="89ed2-123">変更可能なコンテナーにテーブルを制限する DT_MODIFIABLE です。</span><span class="sxs-lookup"><span data-stu-id="89ed2-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="89ed2-124">**PR_ENTRYID**、 **PR_DISPLAY_TYPE**、および興味の他のすべての列を含む[SPropTagArray](sproptagarray.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="89ed2-125">[HrQueryAllRows](hrqueryallrows.md)で、プロパティの制限とプロパティ タグ配列を渡してを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="89ed2-126">**HrQueryAllRows**は、0 個または複数の行、指定した型に属するすべてのコンテナーの 1 つの行が返されます。</span><span class="sxs-lookup"><span data-stu-id="89ed2-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="89ed2-127">行の任意の数の戻り値を処理するために準備します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="89ed2-128">目的のコンテナーを表す行の**PR_ENTRYID**列のエントリの識別子を使用して**アドレス帳コンテナー**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="89ed2-129">場合は、コンテナーを開くには、特定のアドレス帳プロバイダーに属します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="89ed2-130">プロパティ タグ、プロパティの値として、プロバイダー固有の値との関係の RELOP_EQ の**PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) と、 [SPropertyRestriction](spropertyrestriction.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="89ed2-131">通常プロバイダー固有の値は、グローバルに一意の識別子または GUID です。</span><span class="sxs-lookup"><span data-stu-id="89ed2-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="89ed2-132">アドレス帳プロバイダーのヘッダー ファイルのいずれかで公開されているこの値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="89ed2-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="89ed2-133">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_AB_PROVIDERS**、および興味の他のすべての列を含む[SPropTagArray](sproptagarray.md)構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="89ed2-134">[HrQueryAllRows](hrqueryallrows.md)で、プロパティの制限とプロパティ タグ配列を渡してを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="89ed2-135">プロファイルで指定したアドレス帳プロバイダーがない場合は、 **HrQueryAllRows**を 0 個の行に戻ります。</span><span class="sxs-lookup"><span data-stu-id="89ed2-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="89ed2-136">プロバイダーの構成方法に応じて、プロバイダーの最上位のコンテナーの 1 つまたは複数の行を返すことです。</span><span class="sxs-lookup"><span data-stu-id="89ed2-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="89ed2-137">目的のコンテナーを表す行の**PR_ENTRYID**列のエントリの識別子を使用して[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="89ed2-138">興味があることをコンテナーが最上位のコンテナーでない場合は、最上位のコンテナーを検索し、階層を移動します。</span><span class="sxs-lookup"><span data-stu-id="89ed2-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

