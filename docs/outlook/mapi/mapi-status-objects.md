---
title: MAPI 状態オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406746"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="da6d0-103">MAPI 状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="da6d0-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="da6d0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da6d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da6d0-105">Status オブジェクトは、MAPI リソースに関する情報を報告します。</span><span class="sxs-lookup"><span data-stu-id="da6d0-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="da6d0-106">たとえば、サービス プロバイダー、MAPI 送受信プロセス、アドレス帳などです。</span><span class="sxs-lookup"><span data-stu-id="da6d0-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="da6d0-107">現在のプロファイルには、個々のサービス プロバイダーに関する情報を提供する状態オブジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="da6d0-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="da6d0-108">MAPI は、サブシステム、MAPI 送受信プロセス、およびアドレス帳の状態オブジェクトを実装する責任があります。</span><span class="sxs-lookup"><span data-stu-id="da6d0-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="da6d0-109">サブシステムの状態オブジェクトは、グローバル情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="da6d0-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="da6d0-110">統合アドレス帳の status オブジェクトは、現在動作しているすべてのアドレス帳プロバイダーの状態を提供します。</span><span class="sxs-lookup"><span data-stu-id="da6d0-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="da6d0-111">すべての status オブジェクトは、セッションのすべての状態情報をクライアントに提供する MAPI によって管理されるテーブルである状態テーブルに含まれます。</span><span class="sxs-lookup"><span data-stu-id="da6d0-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="da6d0-112">詳細については、「Status [Tables」を参照してください](status-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="da6d0-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="da6d0-113">クライアントは、テーブルまたはサービス プロバイダーのログオン オブジェクトを介して、特定の状態オブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="da6d0-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="da6d0-114">たとえば、アドレス帳プロバイダーの状態オブジェクトにアクセスするために、クライアントは **IABLogon::OpenStatusEntry を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="da6d0-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="da6d0-115">詳細については [、「IABLogon::OpenStatusEntry」を参照してください](iablogon-openstatusentry.md)。</span><span class="sxs-lookup"><span data-stu-id="da6d0-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="da6d0-116">クライアントは、状態オブジェクトを使用して、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="da6d0-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="da6d0-117">セッションの状態について学習します。</span><span class="sxs-lookup"><span data-stu-id="da6d0-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="da6d0-118">サービス プロバイダーを監視します。</span><span class="sxs-lookup"><span data-stu-id="da6d0-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="da6d0-119">メッセージの送信を制御します。</span><span class="sxs-lookup"><span data-stu-id="da6d0-119">Control message transmission.</span></span>
    
- <span data-ttu-id="da6d0-120">リソースの構成と状態を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="da6d0-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="da6d0-121">すべての status オブジェクトは **、IMAPIStatus インターフェイスを実装** します。</span><span class="sxs-lookup"><span data-stu-id="da6d0-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="da6d0-122">詳細については [、「IMAPIStatus : IMAPIProp 」を参照してください](imapistatusimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="da6d0-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="da6d0-123">ただし、すべての状態オブジェクトがすべての **IMAPIStatus メソッドを完全にサポートしているわけではありません** 。</span><span class="sxs-lookup"><span data-stu-id="da6d0-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="da6d0-124">status オブジェクトでサポートされるメソッドにはバリエーションが存在しますので、クライアントは、それを使用する前に、特定の状態オブジェクトについて学習する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da6d0-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="da6d0-125">Status オブジェクトは、次の 3 つのプロパティで機能に関する情報を公開するために必要です。</span><span class="sxs-lookup"><span data-stu-id="da6d0-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="da6d0-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="da6d0-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="da6d0-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="da6d0-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="da6d0-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="da6d0-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="da6d0-129">status オブジェクトの実装の詳細については、「Status [Object Implementation」を参照してください](status-object-implementation.md)。</span><span class="sxs-lookup"><span data-stu-id="da6d0-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="da6d0-130">status オブジェクトの使用の詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="da6d0-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

