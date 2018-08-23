---
title: レプリケーション API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 50b36ee60d00e06a1f5baa8726b5f27c4a3e6ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799597"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="2292a-103">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="2292a-103">About the Replication API</span></span>

  
  
<span data-ttu-id="2292a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2292a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2292a-105">レプリケーション API は、サーバーとプライベート .pst ベース ローカル ストア プロバイダーの作成は、Microsoft Outlook 2013 または Microsoft Outlook 2010 の項目を同期するには、MAPI メッセージ ストア プロバイダーの機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2292a-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2292a-106">MAPI メッセージ ストア プロバイダーは、[レプリケーションの状態マシンについて](about-the-replication-state-machine.md)の手順に従ってレプリケーション API を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2292a-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="2292a-107">プロバイダーは自体には、用に作成された個人用のストアにのみ、API を使用する必要があり、他のプロバイダー用に作成された個人用ストアではなくの個人ストアを作成するため他のプロバイダーが既に設定されているそれぞれのサーバーとのレプリケーション メカニズムを独自します。</span><span class="sxs-lookup"><span data-stu-id="2292a-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="2292a-108">たとえば、オフライン フォルダー ファイル (.ost) は、Microsoft Exchange サーバーとそのレプリケーション ・ リレーションシップを維持します。</span><span class="sxs-lookup"><span data-stu-id="2292a-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="2292a-109">レプリケーション API を使用するには、MAPI メッセージ ストア プロバイダーする必要があります最初を開き**[NSTServiceEntry](nstserviceentry.md)** を呼び出すことによって .pst ベースのローカル ストアをラップします。</span><span class="sxs-lookup"><span data-stu-id="2292a-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="2292a-110">プロバイダーは、レプリケーションを実行するための API、 **[IOSTX](iostxiunknown.md)** **[IPSTX](ipstxiunknown.md)**、主要なインタ フェースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2292a-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="2292a-111">照会することで**IPSTX**が用意されている[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)、 **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**、 **IOSTX**が用意されているとします。</span><span class="sxs-lookup"><span data-stu-id="2292a-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="2292a-112">IOSTX インタ フェース</span><span class="sxs-lookup"><span data-stu-id="2292a-112">The IOSTX Interface</span></span>

<span data-ttu-id="2292a-113">**IOSTX**インターフェイスは、レプリケーション API で同期を実行するプライマリ インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2292a-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="2292a-114">**IOSTX**は、変更をサーバー上のローカル ストアに通知するとともに各状態で、ローカル ストア内の変更に関する情報を取得する一連の状態のローカル ストアを移動します。</span><span class="sxs-lookup"><span data-stu-id="2292a-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="2292a-115">レプリケーション API では、同期をサポートする多くのデータ構造体も指定します。</span><span class="sxs-lookup"><span data-stu-id="2292a-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="2292a-116">ストア プロバイダーでは、この API では、クライアントとして API を使用して、レプリケーション、ローカル ストアをラップし、サーバーに (フォルダー階層、または新しい項目の追加に変更) などのローカル ストアに変更をプッシュし、取得するもこれらの状態間を移動します。**IOSTX**インターフェイスには、その情報を提供するサーバー上の変更に関する情報です。</span><span class="sxs-lookup"><span data-stu-id="2292a-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="2292a-117">**IOSTX**インターフェイスでは、増分変更の同期 (ICS) の Microsoft Exchange Server によって提供されるを適用します。</span><span class="sxs-lookup"><span data-stu-id="2292a-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="2292a-118">ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2292a-118">For more information about ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="2292a-119">**IOSTX**クライアントを使用して ICS を監視し、階層、またはローカル ストア上のコンテンツへの増分変更を同期します。</span><span class="sxs-lookup"><span data-stu-id="2292a-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="2292a-120">IPSTX インタ フェース</span><span class="sxs-lookup"><span data-stu-id="2292a-120">The IPSTX Interface</span></span>

 <span data-ttu-id="2292a-121">**IPSTX**およびその他の 5 * * IPSTX *n* * * **IPSTX**から継承しているインターフェイスは、 **IOSTX**インターフェイスを使用するレプリケーションを実行するときに使用できるヘルパー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2292a-121">**IPSTX** and five other **IPSTX *n* ** interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="2292a-122">たとえば、 **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** を使用すると、サーバーに送信するメッセージをスプールする Outlook プロトコル マネージャーをエミュレートするローカル ストアを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2292a-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="2292a-123">レプリケーション中に状態遷移の詳細については、[レプリケーションの状態マシンの詳細](about-the-replication-state-machine.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2292a-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="2292a-124">レプリケーション API</span><span class="sxs-lookup"><span data-stu-id="2292a-124">The Replication API</span></span>

<span data-ttu-id="2292a-125">レプリケーション API は、次の定義、データ型、およびインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="2292a-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="2292a-126">ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーの実装のサンプル、[についてはサンプル ラップ PST ストア プロバイダー](about-the-sample-wrapped-pst-store-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2292a-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="2292a-127">定義</span><span class="sxs-lookup"><span data-stu-id="2292a-127">Definitions:</span></span>
  
- [<span data-ttu-id="2292a-128">レプリケーション API の定数</span><span class="sxs-lookup"><span data-stu-id="2292a-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="2292a-129">関数</span><span class="sxs-lookup"><span data-stu-id="2292a-129">Functions:</span></span>
  
- <span data-ttu-id="2292a-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="2292a-131">データ型:</span><span class="sxs-lookup"><span data-stu-id="2292a-131">Data types:</span></span>
  
- <span data-ttu-id="2292a-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="2292a-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="2292a-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="2292a-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="2292a-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="2292a-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="2292a-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="2292a-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="2292a-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="2292a-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="2292a-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="2292a-143">**[同期状態](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="2292a-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="2292a-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="2292a-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="2292a-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="2292a-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="2292a-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="2292a-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="2292a-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="2292a-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="2292a-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="2292a-154">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="2292a-154">Interfaces:</span></span>
  
- <span data-ttu-id="2292a-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="2292a-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="2292a-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="2292a-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="2292a-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="2292a-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="2292a-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="2292a-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

