---
title: MAPI オブジェクトのステータス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 69a4d25fc6a7abec68c94cc947e5944322d230a6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594951"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="13490-103">MAPI オブジェクトのステータス</span><span class="sxs-lookup"><span data-stu-id="13490-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="13490-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13490-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13490-105">状態オブジェクトは、MAPI リソースに関する情報をレポートします。</span><span class="sxs-lookup"><span data-stu-id="13490-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="13490-106">などのサービス プロバイダー、MAPI 送信/受信プロセス、またはアドレス帳に。</span><span class="sxs-lookup"><span data-stu-id="13490-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="13490-107">状態オブジェクトが現在のプロファイルで個々 のサービス プロバイダーに関する情報を指定することがあります。</span><span class="sxs-lookup"><span data-stu-id="13490-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="13490-108">MAPI は、サブシステム、MAPI 送信/受信プロセス、およびアドレス帳のステータスのオブジェクトを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13490-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="13490-109">サブシステムの状態オブジェクトは、グローバルな情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="13490-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="13490-110">統合アドレス帳のステータスのオブジェクトには、動作しているすべてのアドレス帳プロバイダーの状態が用意されています。</span><span class="sxs-lookup"><span data-stu-id="13490-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="13490-111">状態テーブルのすべてのセッションの状態情報をクライアントに提供する MAPI によって保持されるテーブルでは、ステータスのすべてのオブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="13490-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="13490-112">詳細については、[ステータス ・ テーブル](status-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13490-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="13490-113">テーブルまたは、サービス プロバイダーに、そのログオン オブジェクトをクライアントは、特定のステータスのオブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="13490-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="13490-114">たとえば、アドレス帳プロバイダーの状態のオブジェクトにアクセスするに、クライアントは**IABLogon::OpenStatusEntry**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="13490-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="13490-115">詳細については、 [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13490-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="13490-116">クライアントは、オブジェクトの状態を使用できます。</span><span class="sxs-lookup"><span data-stu-id="13490-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="13490-117">セッションの状態について説明します。</span><span class="sxs-lookup"><span data-stu-id="13490-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="13490-118">サービス プロバイダーを監視します。</span><span class="sxs-lookup"><span data-stu-id="13490-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="13490-119">メッセージの転送を制御します。</span><span class="sxs-lookup"><span data-stu-id="13490-119">Control message transmission.</span></span>
    
- <span data-ttu-id="13490-120">表示またはリソースの構成とステータスを変更します。</span><span class="sxs-lookup"><span data-stu-id="13490-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="13490-121">ステータスのすべてのオブジェクトは、 **IMAPIStatus**インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="13490-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="13490-122">詳細についてを参照してください[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="13490-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="13490-123">ただし、すべての状態のオブジェクトは完全に**IMAPIStatus**のすべてのメソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="13490-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="13490-124">ステータス オブジェクトでサポートされているメソッドのバリエーションがあるため、クライアントを使用できるようにする前に、特定のステータスのオブジェクトについて説明する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13490-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="13490-125">状態オブジェクトは、次の 3 つのプロパティでその機能についての情報を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13490-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="13490-126">**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13490-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="13490-127">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13490-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="13490-128">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13490-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="13490-129">状態オブジェクトを実装する方法の詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13490-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="13490-130">ステータス オブジェクトの使い方の詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13490-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

