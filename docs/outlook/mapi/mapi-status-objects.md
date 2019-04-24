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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309535"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="c3720-103">MAPI 状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c3720-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="c3720-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3720-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3720-105">Status オブジェクトは、MAPI リソースに関する情報を報告します。</span><span class="sxs-lookup"><span data-stu-id="c3720-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="c3720-106">たとえば、サービスプロバイダー、MAPI の送受信プロセス、またはアドレス帳などです。</span><span class="sxs-lookup"><span data-stu-id="c3720-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="c3720-107">status オブジェクトは、現在のプロファイル内の各サービスプロバイダーに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3720-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="c3720-108">mapi は、サブシステム、mapi の送受信プロセス、およびアドレス帳の状態オブジェクトの実装を担当します。</span><span class="sxs-lookup"><span data-stu-id="c3720-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="c3720-109">サブシステム状態オブジェクトは、グローバル情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3720-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="c3720-110">統合されたアドレス帳の status オブジェクトは、現在動作しているすべてのアドレス帳プロバイダーの状態を提供します。</span><span class="sxs-lookup"><span data-stu-id="c3720-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="c3720-111">すべての status オブジェクトは状態テーブルに含まれています。このテーブルは、セッションのすべてのステータス情報をクライアントに提供する MAPI で保持されます。</span><span class="sxs-lookup"><span data-stu-id="c3720-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="c3720-112">詳細については、「 [Status Tables](status-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3720-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="c3720-113">クライアントは、テーブルまたはサービスプロバイダーの場合は、そのログオンオブジェクトを通じて、特定の状態オブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c3720-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="c3720-114">たとえば、アドレス帳プロバイダーの状態オブジェクトにアクセスするために、クライアントは**IABLogon:: openstatusentry**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="c3720-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="c3720-115">詳細については、「 [IABLogon:: openstatusentry](iablogon-openstatusentry.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3720-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="c3720-116">クライアントは、status オブジェクトを使用して次のことを行えます。</span><span class="sxs-lookup"><span data-stu-id="c3720-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="c3720-117">セッションの状態について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3720-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="c3720-118">サービスプロバイダーを監視します。</span><span class="sxs-lookup"><span data-stu-id="c3720-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="c3720-119">メッセージ送信を制御します。</span><span class="sxs-lookup"><span data-stu-id="c3720-119">Control message transmission.</span></span>
    
- <span data-ttu-id="c3720-120">リソースの構成と状態を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="c3720-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="c3720-121">すべての status オブジェクトは、 **imapistatus**インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="c3720-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="c3720-122">詳細については、「 [imapistatus: imapistatus](imapistatusimapiprop.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3720-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="c3720-123">ただし、すべてのステータスオブジェクトがすべての**imapistatus**メソッドを完全にサポートするわけではありません。</span><span class="sxs-lookup"><span data-stu-id="c3720-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="c3720-124">status オブジェクトでサポートされているメソッドにはバリエーションがあるため、クライアントは、使用する前に、特定の状態オブジェクトについて知る必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3720-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="c3720-125">状態オブジェクトは、それぞれの機能に関する情報を次の3つのプロパティに公開するために必要です。</span><span class="sxs-lookup"><span data-stu-id="c3720-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="c3720-126">**PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3720-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="c3720-127">**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3720-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="c3720-128">**PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c3720-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="c3720-129">状態オブジェクトの実装の詳細については、「 [status オブジェクトの実装](status-object-implementation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3720-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="c3720-130">status オブジェクトの使用の詳細については、「 [status Table and status Objects](status-table-and-status-objects.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3720-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

