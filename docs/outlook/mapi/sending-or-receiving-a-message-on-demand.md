---
title: 要求時にメッセージを送受信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 668e1c57c59bf2356be808e0347e1bd5135478a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563892"
---
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="57a60-103">要求時にメッセージを送受信します。</span><span class="sxs-lookup"><span data-stu-id="57a60-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="57a60-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57a60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57a60-105">通常、クライアントは、MAPI サブシステムに依存して、MAPI スプーラーとサービス ・ プロバイダー-メッセージの送信と受信のタイミングを処理するために。</span><span class="sxs-lookup"><span data-stu-id="57a60-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="57a60-106">ただし、MAPI スプーラーを無効またはトランスポート プロバイダーのいずれかの状態オブジェクトを使用して、このタイミングを変更できます。</span><span class="sxs-lookup"><span data-stu-id="57a60-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="57a60-107">[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドでは、1 つまたは複数トランスポート プロバイダーの受信または送信キューからすべてのメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="57a60-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="57a60-108">次の手順では、要求時にメッセージを送受信するための 2 つの手法について説明します。</span><span class="sxs-lookup"><span data-stu-id="57a60-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="57a60-109">最初の手順は、プロファイル内のすべてのトランスポート プロバイダーのキューをフラッシュするのには、MAPI スプーラーを無効の状態のオブジェクトを使用してください。2 番目の手順では、1 つのトランスポート プロバイダーのキューをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="57a60-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="57a60-110">1 回の操作ですべての着信または発信キューをフラッシュするには</span><span class="sxs-lookup"><span data-stu-id="57a60-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="57a60-111">ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57a60-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="57a60-112">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) と**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) に設定する列を制限するのには、状態テーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57a60-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="57a60-113">[SPropertyRestriction](spropertyrestriction.md)構造体を使用して、MAPI_SPOOLER と**PR_RESOURCE_TYPE**を一致するようにプロパティ制約を作成します。</span><span class="sxs-lookup"><span data-stu-id="57a60-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="57a60-114">[HrQueryAllRows](hrqueryallrows.md)、 **SPropertyRestriction**構造体を渡すことを呼び出し、MAPI スプーラーを無効の状態を表す行を取得するのには。</span><span class="sxs-lookup"><span data-stu-id="57a60-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="57a60-115">**PR_ENTRYID**の列を MAPI スプーラーを無効の状態のオブジェクトを開くには、 [IMAPISession::OpenEntry](imapisession-openentry.md)に渡します。</span><span class="sxs-lookup"><span data-stu-id="57a60-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="57a60-116">FLUSH_NO_UI フラグをユーザー インターフェイスを非表示にして、送信または受信キューをフラッシュするのには FLUSH_DOWNLOAD または FLUSH_UPLOAD のいずれかのフラグを渡す、MAPI スプーラーの[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57a60-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="57a60-117">状態オブジェクト、状態テーブルとテーブルに割り当てられている[SRowSet](srowset.md)構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="57a60-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="57a60-118">トランスポート プロバイダーによって個別に着信または発信のキューをフラッシュするには</span><span class="sxs-lookup"><span data-stu-id="57a60-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="57a60-119">ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57a60-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="57a60-120">**PR_ENTRYID**と**PR_RESOURCE_TYPE**に設定する列を制限するのには、状態テーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57a60-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="57a60-121">[SPropertyRestriction](spropertyrestriction.md)構造体を使用して、MAPI_TRANSPORT_PROVIDER と**PR_RESOURCE_TYPE**を一致するようにプロパティ制約を作成します。</span><span class="sxs-lookup"><span data-stu-id="57a60-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="57a60-122">[HrQueryAllRows](hrqueryallrows.md)、 **SPropertyRestriction**構造体を渡してトランスポート プロバイダーによって提供されている行を取得するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57a60-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="57a60-123">行ごとに、 **HrQueryAllRows**から返されます。</span><span class="sxs-lookup"><span data-stu-id="57a60-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="57a60-124">**PR_ENTRYID**の列をトランスポート プロバイダーの状態のオブジェクトを開くには、 [IMAPISession::OpenEntry](imapisession-openentry.md)に渡します。</span><span class="sxs-lookup"><span data-stu-id="57a60-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="57a60-125">トランスポートの状態のオブジェクトが、 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティが、STATUS_FLUSH_QUEUES を持っているかを確認することで**FlushQueues**メソッドをサポートすることを確認してフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="57a60-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="57a60-126">サポートされている場合は、 [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57a60-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="57a60-127">サポートされていない場合、は、 _lpTargetTransport_パラメーターで、トランスポートのエントリの識別子を渡す、MAPI スプーラーの**IMAPIStatus::FlushQueues**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57a60-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="57a60-128">MAPI スプーラーを無効の状態のオブジェクトにアクセスする手順については上記の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57a60-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="57a60-129">発信キューをフラッシュするのには FLUSH_DOWNLOAD フラグまたは受信キューをフラッシュするのには FLUSH_UPLOAD フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="57a60-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="57a60-130">状態オブジェクト、状態テーブルとテーブルに割り当てられている[SRowSet](srowset.md)構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="57a60-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="57a60-131">LAN トランスポート プロバイダーのほとんどのように FLUSH_NO_UI フラグは、MAPI スプーラーです。</span><span class="sxs-lookup"><span data-stu-id="57a60-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="57a60-132">ただし、すべてのトランスポート プロバイダーは、このフラグは、特に明示的にモデムを使用して、リモート アクセス サービス (RAS) を優先します。</span><span class="sxs-lookup"><span data-stu-id="57a60-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="57a60-133">RAS は、クライアントがユーザー インターフェイスを非表示にできるように意図していません。</span><span class="sxs-lookup"><span data-stu-id="57a60-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="57a60-134">クライアントで、ユーザーとのやり取りを必要とせずに接続できるが、ことは困難であり、クライアントのメッセージ サービスの詳細な知識を必要とするように構成することができます。</span><span class="sxs-lookup"><span data-stu-id="57a60-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

