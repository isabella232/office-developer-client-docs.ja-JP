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
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="23a57-103">必要に応じてメッセージを送信または受信</span><span class="sxs-lookup"><span data-stu-id="23a57-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="23a57-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23a57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23a57-105">クライアントは通常、MAPI サブシステム (MAPI スプーラーとサービス プロバイダー) を使用して、メッセージの送受信のタイミングを処理します。</span><span class="sxs-lookup"><span data-stu-id="23a57-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="23a57-106">ただし、MAPI スプーラーまたはトランスポート プロバイダーの status オブジェクトを使用して、このタイミングを変更できます。</span><span class="sxs-lookup"><span data-stu-id="23a57-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="23a57-107">[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドは、1 つ以上のトランスポート プロバイダーの受信キューまたは送信キューからすべてのメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="23a57-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="23a57-108">次の手順では、オンデマンドでメッセージを送受信する 2 つの手法について説明します。</span><span class="sxs-lookup"><span data-stu-id="23a57-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="23a57-109">最初の手順では、MAPI スプーラーの status オブジェクトを使用して、プロファイル内のすべてのトランスポート プロバイダーのキューをフラッシュします。2 番目の手順では、1 つのトランスポート プロバイダーのキューをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="23a57-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="23a57-110">1 回の操作ですべての受信キューまたは送信キューをフラッシュするには</span><span class="sxs-lookup"><span data-stu-id="23a57-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="23a57-111">[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="23a57-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="23a57-112">状態テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) および **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))**に** 制限します。</span><span class="sxs-lookup"><span data-stu-id="23a57-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="23a57-113">[SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を構築し、プロパティと **PR_RESOURCE_TYPE一致** MAPI_SPOOLER。</span><span class="sxs-lookup"><span data-stu-id="23a57-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="23a57-114">[HrQueryAllRows](hrqueryallrows.md)を呼び出し **、SPropertyRestriction** 構造体を渡して、MAPI スプーラーの状態を表す行を取得します。</span><span class="sxs-lookup"><span data-stu-id="23a57-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="23a57-115">MAPI ス **プー PR_ENTRYID** の状態オブジェクトを開く場合は、この列を [IMAPISession::OpenEntry](imapisession-openentry.md) に渡します。</span><span class="sxs-lookup"><span data-stu-id="23a57-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="23a57-116">MAPI スプーラーの [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) メソッドを呼び出し、FLUSH_NO_UI フラグを渡してユーザー インターフェイスを抑制し、FLUSH_DOWNLOAD または FLUSH_UPLOAD フラグを使用して送信キューまたは着信キューをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="23a57-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="23a57-117">status オブジェクトと状態テーブル、およびテーブルに割り当てられている [SRowSet](srowset.md) 構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="23a57-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="23a57-118">トランスポート プロバイダーによって受信キューまたは送信キューを個別にフラッシュするには</span><span class="sxs-lookup"><span data-stu-id="23a57-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="23a57-119">[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="23a57-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="23a57-120">状態テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを列セットの値 **PR_ENTRYIDおよび** PR_RESOURCE_TYPE。</span><span class="sxs-lookup"><span data-stu-id="23a57-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="23a57-121">[SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を構築し、プロパティと **PR_RESOURCE_TYPE一致** MAPI_TRANSPORT_PROVIDER。</span><span class="sxs-lookup"><span data-stu-id="23a57-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="23a57-122">[HrQueryAllRows](hrqueryallrows.md)を呼び出し **、SPropertyRestriction** 構造体を渡して、トランスポート プロバイダーによって提供される行を取得します。</span><span class="sxs-lookup"><span data-stu-id="23a57-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="23a57-123">**HrQueryAllRows** から返される各行について、</span><span class="sxs-lookup"><span data-stu-id="23a57-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="23a57-124">**[PR_ENTRYID]** 列を [IMAPISession::OpenEntry](imapisession-openentry.md)に渡して、トランスポート プロバイダーの状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="23a57-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="23a57-125">トランスポート状態オブジェクトが **FlushQueues** メソッドをサポートしている場合は **、PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_FLUSH_QUEUES フラグが設定STATUS_FLUSH_QUEUES確認します。</span><span class="sxs-lookup"><span data-stu-id="23a57-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="23a57-126">サポートされている場合は [、IMAPIStatus::FlushQueues を呼び出します](imapistatus-flushqueues.md)。</span><span class="sxs-lookup"><span data-stu-id="23a57-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="23a57-127">サポートされていない場合は、MAPI スプーラーの **IMAPIStatus::FlushQueues** メソッドを呼び出し  _、lpTargetTransport_ パラメーターでトランスポートのエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="23a57-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="23a57-128">MAPI スプーラーの状態オブジェクトにアクセスする手順については、前の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23a57-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="23a57-129">送信キュー FLUSH_DOWNLOADフラッシュする場合は FLUSH_UPLOADフラグを設定して、受信キューをフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="23a57-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="23a57-130">status オブジェクトと状態テーブル、およびテーブルに割り当てられている [SRowSet](srowset.md) 構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="23a57-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="23a57-131">MAPI スプーラーは、ほとんどの LAN FLUSH_NO_UIと同様に、このフラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="23a57-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="23a57-132">ただし、すべてのトランスポート プロバイダーが、特に明示的にモデムとリモート アクセス サービス (RAS) を使用する場合は、このフラグを受け入れるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="23a57-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="23a57-133">RAS は、クライアントがユーザー インターフェイスを抑制するように設計されていない。</span><span class="sxs-lookup"><span data-stu-id="23a57-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="23a57-134">ユーザーの操作を必要とせずに接続できるようクライアントを構成することは可能ですが、難しく、クライアントのメッセージ サービスに関する深い知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="23a57-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

