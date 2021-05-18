---
title: レプリケーション API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329520"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="1e449-103">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="1e449-103">About the Replication API</span></span>

  
  
<span data-ttu-id="1e449-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e449-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e449-105">レプリケーション API は、MAPI メッセージ ストア プロバイダーがサーバーと、そのプロバイダー用に作成されたプライベートの .pst ベースのローカル ストアとの間で Microsoft Outlook 2013 または Microsoft Outlook 2010 アイテムを同期する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="1e449-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1e449-106">MAPI メッセージ ストア プロバイダーは、「レプリケーション ステート マシンについて」の手順に従ってレプリケーション API [を実装する必要があります](about-the-replication-state-machine.md)。</span><span class="sxs-lookup"><span data-stu-id="1e449-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="1e449-107">プロバイダーは、他のプロバイダー用に作成された個人用ストアが、既にそれぞれのサーバーで独自のレプリケーション メカニズムを設定している可能性があるため、他のプロバイダー用に作成された個人用ストアではなく、自身用に作成された個人用ストアでのみ API を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e449-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="1e449-108">たとえば、オフライン フォルダー ファイル (.ost) は、Microsoft サーバーと独自のレプリケーションExchangeします。</span><span class="sxs-lookup"><span data-stu-id="1e449-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="1e449-109">レプリケーション API を使用するには、MAPI メッセージ ストア プロバイダーが **[NSTServiceEntry](nstserviceentry.md)** を呼び出して .pst ベースのローカル ストアを開いてラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e449-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="1e449-110">プロバイダーは **[、API、IOSTX、IPSTX](iostxiunknown.md)** の主要なインターフェイス **[](ipstxiunknown.md)** を使用してレプリケーションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="1e449-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="1e449-111">**IPSTX** は [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)でのクエリによって提供され **、IOSTX** は **[IPSTX::GetSyncObject によって提供されます](ipstx-getsyncobject.md)**。</span><span class="sxs-lookup"><span data-stu-id="1e449-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="1e449-112">IOSTX インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1e449-112">The IOSTX Interface</span></span>

<span data-ttu-id="1e449-113">**IOSTX インターフェイス** は、レプリケーション API で同期を実行するプライマリ インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="1e449-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="1e449-114">**IOSTX** は、一連の状態を通じてローカル ストアを移動し、ローカル ストアの変更に関する各状態の情報を取得し、サーバー上の変更をローカル ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="1e449-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="1e449-115">レプリケーション API では、同期をサポートする多くのデータ構造も指定します。</span><span class="sxs-lookup"><span data-stu-id="1e449-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="1e449-116">ストア プロバイダーは、この API のクライアントとして、レプリケーション API を使用してローカル ストアをラップし、これらの状態を移動し、ローカル ストアでの変更 (フォルダー階層の変更や新しいアイテムの追加など) をサーバーにプッシュし、サーバー上の変更に関する情報を取得し、その情報を **IOSTX** インターフェイスに提供します。</span><span class="sxs-lookup"><span data-stu-id="1e449-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="1e449-117">**IOSTX インターフェイスは**、ユーザーが提供する増分変更同期 (ICS) をMicrosoft Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="1e449-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="1e449-118">ICS の詳細については [、「ICS 評価基準」を参照してください](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1e449-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="1e449-119">**IOSTX を介** して、クライアントは ICS を使用して、ローカル ストア上の階層またはコンテンツに対する増分変更を監視および同期します。</span><span class="sxs-lookup"><span data-stu-id="1e449-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="1e449-120">IPSTX インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1e449-120">The IPSTX Interface</span></span>

 <span data-ttu-id="1e449-121">**IPSTX および** IPSTXから継承する他の 5 つの \*\*\*\*IPSTX\*\* n \*\* インターフェイスは **、IOSTX** インターフェイスを介してレプリケーションを実行するときに使用できるヘルパー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="1e449-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="1e449-122">たとえば **[、IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** を使用すると、ローカル ストアで Outlook プロトコル マネージャーをエミュレートして、送信メッセージをサーバーにスプールできます。</span><span class="sxs-lookup"><span data-stu-id="1e449-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="1e449-123">レプリケーション中の状態遷移の詳細については、「レプリケーションステート マシンについて [」を参照してください](about-the-replication-state-machine.md)。</span><span class="sxs-lookup"><span data-stu-id="1e449-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="1e449-124">レプリケーション API</span><span class="sxs-lookup"><span data-stu-id="1e449-124">The Replication API</span></span>

<span data-ttu-id="1e449-125">レプリケーション API には、次の定義、データ型、およびインターフェイスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e449-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="1e449-126">ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーの実装例については、「サンプル ラップされた PST ストア プロバイダーについて」 [を参照してください](about-the-sample-wrapped-pst-store-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="1e449-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="1e449-127">定義:</span><span class="sxs-lookup"><span data-stu-id="1e449-127">Definitions:</span></span>
  
- [<span data-ttu-id="1e449-128">レプリケーション API の定数</span><span class="sxs-lookup"><span data-stu-id="1e449-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="1e449-129">関数</span><span class="sxs-lookup"><span data-stu-id="1e449-129">Functions:</span></span>
  
- <span data-ttu-id="1e449-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="1e449-131">データ型:</span><span class="sxs-lookup"><span data-stu-id="1e449-131">Data types:</span></span>
  
- <span data-ttu-id="1e449-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="1e449-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="1e449-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="1e449-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="1e449-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="1e449-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="1e449-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="1e449-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="1e449-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="1e449-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="1e449-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="1e449-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="1e449-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="1e449-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="1e449-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="1e449-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="1e449-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="1e449-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="1e449-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="1e449-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="1e449-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="1e449-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="1e449-154">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="1e449-154">Interfaces:</span></span>
  
- <span data-ttu-id="1e449-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="1e449-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="1e449-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="1e449-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="1e449-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="1e449-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="1e449-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="1e449-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

