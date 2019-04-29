---
title: 必要に応じてメッセージを送信または受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436371"
---
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="f50f4-103">必要に応じてメッセージを送信または受信</span><span class="sxs-lookup"><span data-stu-id="f50f4-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="f50f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f50f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f50f4-105">通常、クライアントは mapi サブシステム (mapi スプーラーおよびサービスプロバイダー) に依存して、メッセージの送信と受信のタイミングを処理します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="f50f4-106">ただし、このタイミングは、MAPI スプーラーまたはトランスポートプロバイダーの status オブジェクトを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="f50f4-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="f50f4-107">[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドは、1つ以上のトランスポートプロバイダーの受信キューまたは送信キューからすべてのメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="f50f4-108">次の手順では、オンデマンドでメッセージを送受信する2つの方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="f50f4-109">最初の手順では、MAPI スプーラーの status オブジェクトを使用して、プロファイル内のすべてのトランスポートプロバイダーのキューをフラッシュします。2番目のプロシージャは、1つのトランスポートプロバイダーのキューをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="f50f4-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="f50f4-110">1回の操作ですべての着信または発信キューをフラッシュするには</span><span class="sxs-lookup"><span data-stu-id="f50f4-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="f50f4-111">呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f50f4-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="f50f4-112">状態テーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) および**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) に制限します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="f50f4-113">**PR_RESOURCE_TYPE**と MAPI_SPOOLER を一致させるために、 [spropertyrestriction](spropertyrestriction.md)構造を使用してプロパティ制限を構築します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="f50f4-114">MAPI スプーラーの状態を表す行を取得するには、 [hrqueryallrows](hrqueryallrows.md)を呼び出し、 **spropertyrestriction**構造を渡します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="f50f4-115">**PR_ENTRYID**列を[imapisession:: openentry](imapisession-openentry.md)に渡して、MAPI スプーラーの status オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="f50f4-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="f50f4-116">MAPI スプーラーの[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドを呼び出し、FLUSH_NO_UI フラグを渡してユーザーインターフェイスを非表示にし、送信または受信キューをフラッシュする FLUSH_DOWNLOAD または FLUSH_UPLOAD フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="f50f4-117">status オブジェクトと状態テーブルを解放します。また、テーブルに割り当てられている[srowset](srowset.md)構造も解放します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="f50f4-118">着信または発信キューをトランスポートプロバイダーによって個別にフラッシュするには</span><span class="sxs-lookup"><span data-stu-id="f50f4-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="f50f4-119">呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f50f4-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="f50f4-120">状態テーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列が**PR_ENTRYID**と**PR_RESOURCE_TYPE**に設定されるように制限します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="f50f4-121">**PR_RESOURCE_TYPE**と MAPI_TRANSPORT_PROVIDER を一致させるために、 [spropertyrestriction](spropertyrestriction.md)構造を使用してプロパティ制限を構築します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="f50f4-122">トランスポートプロバイダーによって提供される行を取得するには、 [hrqueryallrows](hrqueryallrows.md)を呼び出し、 **spropertyrestriction**構造を渡します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="f50f4-123">**hrqueryallrows**から返される各行ごとに、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="f50f4-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="f50f4-124">**PR_ENTRYID**列を[imapisession:: openentry](imapisession-openentry.md)に渡して、トランスポートプロバイダーの status オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="f50f4-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="f50f4-125">トランスポート状態オブジェクトが、 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_FLUSH_QUEUES フラグが設定されていることを確認して、 **flushqueues**メソッドをサポートしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f50f4-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="f50f4-126">サポートされている場合は、 [imapistatus:: flushqueues](imapistatus-flushqueues.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="f50f4-127">サポートされていない場合は、MAPI スプーラーの**imapistatus:: flushqueues**メソッドを呼び出して、 _lptargettransport_パラメーターでトランスポートのエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="f50f4-128">MAPI スプーラーの状態オブジェクトにアクセスする手順については、前の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f50f4-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="f50f4-129">送信キューまたは FLUSH_UPLOAD フラグをフラッシュして、受信キューをフラッシュするように FLUSH_DOWNLOAD フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="f50f4-130">status オブジェクトと状態テーブルを解放します。また、テーブルに割り当てられている[srowset](srowset.md)構造も解放します。</span><span class="sxs-lookup"><span data-stu-id="f50f4-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="f50f4-131">MAPI スプーラーは、ほとんどの LAN トランスポートプロバイダーと同様に FLUSH_NO_UI フラグを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="f50f4-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="f50f4-132">ただし、すべてのトランスポートプロバイダーがこのフラグを使用するわけではありません。特に、モデムを明示的に使用するものやリモートアクセスサービス (RAS) を使用するものもあります。</span><span class="sxs-lookup"><span data-stu-id="f50f4-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="f50f4-133">RAS は、クライアントがユーザーインターフェイスを抑制することを許可するようには設計されていません。</span><span class="sxs-lookup"><span data-stu-id="f50f4-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="f50f4-134">クライアントがユーザーの操作を必要とせずに接続できるように、クライアントを構成することは可能ですが、これは困難で、クライアントのメッセージサービスを熟知している必要があります。</span><span class="sxs-lookup"><span data-stu-id="f50f4-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

