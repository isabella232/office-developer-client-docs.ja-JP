---
title: アドレス帳のコンテナーを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326580"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="2a8f2-103">アドレス帳のコンテナーを開く</span><span class="sxs-lookup"><span data-stu-id="2a8f2-103">Opening an address book container</span></span>

<span data-ttu-id="2a8f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a8f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a8f2-105">MAPI 統合アドレス帳を開いたら、1つ以上のアドレス帳コンテナーを開いて、その内部の受信者にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="2a8f2-106">アドレス帳のトップレベルのコンテナーを開くには、NULL エントリ識別子を持つ[IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="2a8f2-107">アドレス帳コンテナーは、読み取り専用または読み取り/書き込みアクセスで実装できます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="2a8f2-108">読み取り専用コンテナーは、参照にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="2a8f2-109">読み取り/書き込みコンテナーを変更して、クライアントが新しいエントリを作成したり、既存のエントリを削除したり、変更したりできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="2a8f2-110">すべての個人用アドレス帳 (PAB) コンテナーは、読み取り/書き込みコンテナーとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="2a8f2-111">任意の下位レベルのコンテナーを開くには、 **openentry**を呼び出し、開くコンテナーのエントリ識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="2a8f2-112">PAB として指定されたコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="2a8f2-113">[IAddrBook:: getpab](iaddrbook-getpab.md)を呼び出して、pab のエントリ識別子を取得します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="2a8f2-114">このエントリ識別子を[IAddrBook:: openentry](iaddrbook-openentry.md)に渡します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="2a8f2-115">PAB ではないコンテナーを開く</span><span class="sxs-lookup"><span data-stu-id="2a8f2-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="2a8f2-116">[IAddrBook::](iaddrbook-openentry.md) NULL エントリ識別子を持つ openentry を呼び出して、アドレス帳のルートコンテナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="2a8f2-117">ルートコンテナーの[IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md)メソッドを呼び出して、その階層テーブルを取得します。これには、アドレス帳のすべてのトップレベルコンテナーのリストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="2a8f2-118">開くコンテナーが特定の種類の場合:</span><span class="sxs-lookup"><span data-stu-id="2a8f2-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="2a8f2-119">プロパティタグ、プロパティ値のコンテナーの種類、およびリレーションシップの RELOP_EQ に対して、 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) を使用して**spropertyrestriction**構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="2a8f2-120">**PR_DISPLAY_TYPE**には、複数の値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="2a8f2-121">DT_GLOBAL は、階層テーブルをグローバルアドレス一覧に含まれるコンテナーに制限します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="2a8f2-122">DT_LOCAL は、ローカルアドレス帳に属するコンテナーにテーブルを制限します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="2a8f2-123">DT_MODIFIABLE を使用して、変更可能なコンテナーにテーブルを制限します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="2a8f2-124">**PR_ENTRYID**、 **PR_DISPLAY_TYPE**、およびその他の目的の列を含む[SPropTagArray](sproptagarray.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="2a8f2-125">[hrqueryallrows](hrqueryallrows.md)を呼び出し、プロパティの制限とプロパティタグの配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="2a8f2-126">**hrqueryallrows**は、0個以上の行を返します。これは、指定された種類に属するすべてのコンテナーにつき1行です。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="2a8f2-127">任意の数の行の戻り値を処理できるように準備します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="2a8f2-128">目的のコンテナーを表す行の**PR_ENTRYID**列から、エントリ識別子を持つ**IAddrBook:: openentry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="2a8f2-129">開くコンテナーが特定のアドレス帳プロバイダーに属している場合:</span><span class="sxs-lookup"><span data-stu-id="2a8f2-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="2a8f2-130">プロパティタグに対して**PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) を使用して[spropertyrestriction](spropertyrestriction.md)構造を作成し、プロパティ値にプロバイダー固有の値を指定し、リレーションシップに RELOP_EQ を指定します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="2a8f2-131">通常、プロバイダー固有の値は、グローバルに一意の識別子または GUID です。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="2a8f2-132">この値は、アドレス帳プロバイダーのヘッダーファイルのいずれかに公開されています。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="2a8f2-133">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_AB_PROVIDERS**、およびその他の目的の列を含む[SPropTagArray](sproptagarray.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="2a8f2-134">[hrqueryallrows](hrqueryallrows.md)を呼び出し、プロパティの制限とプロパティタグの配列を渡します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="2a8f2-135">指定したアドレス帳プロバイダーがプロファイルにない場合、 **hrqueryallrows**は0行を返します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="2a8f2-136">プロバイダーがどのように編成されているかに応じて、プロバイダーの最上位のコンテナーに対して1つ以上の行を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="2a8f2-137">目的のコンテナーを表す行の**PR_ENTRYID**列から、エントリ識別子を持つ[IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="2a8f2-138">目的のコンテナーが最上位のコンテナーではない場合は、最上位のコンテナーを見つけて、階層をスキャンします。</span><span class="sxs-lookup"><span data-stu-id="2a8f2-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

