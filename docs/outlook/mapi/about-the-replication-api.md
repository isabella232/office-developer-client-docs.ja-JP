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
# <a name="about-the-replication-api"></a><span data-ttu-id="a3569-103">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a3569-103">About the Replication API</span></span>

  
  
<span data-ttu-id="a3569-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3569-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3569-105">レプリケーション API は、MAPI メッセージストアプロバイダーが、microsoft outlook 2013 または microsoft outlook 2010 アイテムを、そのプロバイダに対して作成されたサーバーとプライベート .pst ベースのローカルストアとの間で同期する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="a3569-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a3569-106">MAPI メッセージストアプロバイダーは、[レプリケーション状態マシンについて](about-the-replication-state-machine.md)の指示に従って、レプリケーション API を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3569-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="a3569-107">プロバイダーは、他のプロバイダー用に作成された個人用ストアに対してのみ API を使用する必要があります。他のプロバイダー用に作成された個人用ストアでは、それぞれのサーバーに対して独自のレプリケーションメカニズムが既にセットアップされている場合があるためです。</span><span class="sxs-lookup"><span data-stu-id="a3569-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="a3569-108">たとえば、オフラインフォルダーファイル (.ost) は、Microsoft Exchange サーバーとの間でレプリケーション関係を維持します。</span><span class="sxs-lookup"><span data-stu-id="a3569-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="a3569-109">レプリケーション API を使用するには、最初に**[nstserviceentry](nstserviceentry.md)** を呼び出すことによって、MAPI メッセージストアプロバイダーが .pst ベースのローカルストアを開いてラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3569-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="a3569-110">プロバイダーは、API の主なインターフェイスである**[iostx](iostxiunknown.md)** と**[ipstx](ipstxiunknown.md)** を使用して、レプリケーションを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="a3569-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="a3569-111">**ipstx**は、IMsgStore に対するクエリによって提供され[ます。 imapiprop](imsgstoreimapiprop.md)、および**[GetSyncObject](ipstx-getsyncobject.md)** によって**iostx**が提供されます。</span><span class="sxs-lookup"><span data-stu-id="a3569-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="a3569-112">iostx インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3569-112">The IOSTX Interface</span></span>

<span data-ttu-id="a3569-113">**iostx**インターフェイスは、レプリケーション API で同期を実行するプライマリインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="a3569-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="a3569-114">**iostx**ローカルストアを一連の状態で移動し、ローカルストアの変更に関する各状態の情報を取得します。また、サーバー上の変更をローカルストアに通知することもできます。</span><span class="sxs-lookup"><span data-stu-id="a3569-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="a3569-115">レプリケーション API でも、同期をサポートする多くのデータ構造が指定されています。</span><span class="sxs-lookup"><span data-stu-id="a3569-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="a3569-116">この api のクライアントとしてのストアプロバイダーは、レプリケーション API を使用して、ローカルストアをラップし、これらの状態を使用して、ローカルストアに対する変更 (フォルダー階層への変更、新しいアイテムの追加など) をサーバーにプッシュします。また、サーバー上の変更に関する情報と、その情報を**iostx**インターフェイスに提供します。</span><span class="sxs-lookup"><span data-stu-id="a3569-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="a3569-117">**iostx**インターフェイスは、Microsoft Exchange Server によって提供される増分変更同期 (ICS) を採用します。</span><span class="sxs-lookup"><span data-stu-id="a3569-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="a3569-118">ics の詳細については、「 [ics の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3569-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="a3569-119">**iostx**を使用すると、クライアントは ICS を使用して、ローカルストア上の階層またはコンテンツに対する増分の変更を監視し、同期します。</span><span class="sxs-lookup"><span data-stu-id="a3569-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="a3569-120">ipstx インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3569-120">The IPSTX Interface</span></span>

 <span data-ttu-id="a3569-121">\*\*\*\* ipstx およびその他の5つの \* \* ipstx n \* \* \*\*\*\* ipstx *n* \* \* は、 **iostx**インターフェイスを介してレプリケーションを実行するときに使用できるヘルパー機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="a3569-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="a3569-122">たとえば、 **[ipstx:: EmulateSpooler](ipstx-emulatespooler.md)** を使用すると、ローカルストアが Outlook プロトコルマネージャーをエミュレートして、送信メッセージをサーバーにスプールするようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a3569-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="a3569-123">レプリケーション中の状態遷移の詳細については、「 [replication state Machine につい](about-the-replication-state-machine.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3569-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="a3569-124">レプリケーション API</span><span class="sxs-lookup"><span data-stu-id="a3569-124">The Replication API</span></span>

<span data-ttu-id="a3569-125">レプリケーション API は、次の日、データ型、およびインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="a3569-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="a3569-126">ラップされた個人用フォルダーファイル (PST) のストアプロバイダーのサンプルの実装については、「[サンプルのラップされた PST ストアプロバイダーについ](about-the-sample-wrapped-pst-store-provider.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3569-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="a3569-127">定義</span><span class="sxs-lookup"><span data-stu-id="a3569-127">Definitions:</span></span>
  
- [<span data-ttu-id="a3569-128">レプリケーション API の定数</span><span class="sxs-lookup"><span data-stu-id="a3569-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="a3569-129">関数</span><span class="sxs-lookup"><span data-stu-id="a3569-129">Functions:</span></span>
  
- <span data-ttu-id="a3569-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="a3569-131">データ型:</span><span class="sxs-lookup"><span data-stu-id="a3569-131">Data types:</span></span>
  
- <span data-ttu-id="a3569-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="a3569-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="a3569-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="a3569-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="a3569-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="a3569-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="a3569-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="a3569-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="a3569-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="a3569-141">**[頻度](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="a3569-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="a3569-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="a3569-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="a3569-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="a3569-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="a3569-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="a3569-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="a3569-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="a3569-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="a3569-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="a3569-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="a3569-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="a3569-154">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a3569-154">Interfaces:</span></span>
  
- <span data-ttu-id="a3569-155">**[iostx](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="a3569-156">**[ipstx](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="a3569-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="a3569-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="a3569-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="a3569-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="a3569-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="a3569-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

