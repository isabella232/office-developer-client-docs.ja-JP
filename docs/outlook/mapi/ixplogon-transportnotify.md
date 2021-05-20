---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2482dc39d3f1d1568b45dd3de88358e08d190be4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428859"
---
# <a name="ixplogontransportnotify"></a><span data-ttu-id="159ed-103">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="159ed-103">IXPLogon::TransportNotify</span></span>

<span data-ttu-id="159ed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="159ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="159ed-105">トランスポート プロバイダーが通知を要求したイベントの発生を通知します。</span><span class="sxs-lookup"><span data-stu-id="159ed-105">Signals the occurrence of an event about which the transport provider requested notification.</span></span>
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a><span data-ttu-id="159ed-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="159ed-106">Parameters</span></span>

 <span data-ttu-id="159ed-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="159ed-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="159ed-108">[in, out]通知イベントを通知するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="159ed-108">[in, out] A bitmask of flags that signals notification events.</span></span> <span data-ttu-id="159ed-109">次のフラグは、入力時に MAPI スプーラーによって設定できます。出力時に変更されずに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-109">The following flags can be set by the MAPI spooler on input and must be returned unchanged on output:</span></span>
    
<span data-ttu-id="159ed-110">NOTIFY_ABORT_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="159ed-110">NOTIFY_ABORT_DEFERRED</span></span> 
  
> <span data-ttu-id="159ed-111">トランスポート プロバイダーに、責任を受け入れるメッセージが延期されたと通知します。</span><span class="sxs-lookup"><span data-stu-id="159ed-111">Notifies the transport provider that a message for which it accepted responsibility is being deferred.</span></span> <span data-ttu-id="159ed-112">遅延をサポートするトランスポート プロバイダーだけが、このフラグをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-112">Only transport providers that support deferral must support this flag.</span></span> <span data-ttu-id="159ed-113">_lppvData パラメーター_ は、取り消されたメッセージのエントリ識別子をポイントします。</span><span class="sxs-lookup"><span data-stu-id="159ed-113">The  _lppvData_ parameter points to the entry identifier of the canceled message.</span></span> <span data-ttu-id="159ed-114">MAPI スプーラーが処理していないメッセージは [、IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) メソッドを呼び出すことによって、引き続き延期できます。</span><span class="sxs-lookup"><span data-stu-id="159ed-114">Messages that the MAPI spooler has not processed can still be deferred by calling the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method.</span></span> 
    
<span data-ttu-id="159ed-115">NOTIFY_BEGIN_INBOUND</span><span class="sxs-lookup"><span data-stu-id="159ed-115">NOTIFY_BEGIN_INBOUND</span></span> 
  
> <span data-ttu-id="159ed-116">MAPI スプーラーは、このトランスポート プロバイダー セッションの受信メッセージを受け入れ可能になります。</span><span class="sxs-lookup"><span data-stu-id="159ed-116">The MAPI spooler can now accept inbound messages for this transport provider session.</span></span> <span data-ttu-id="159ed-117">MAPI スプーラーは、トランスポート プロバイダーがログオン時に[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)呼び出しで LOGON_SP_POLL フラグを設定した場合、定期的に[IXPLogon::P oll](ixplogon-poll.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="159ed-117">The MAPI spooler regularly calls the [IXPLogon::Poll](ixplogon-poll.md) method if the transport provider set the LOGON_SP_POLL flag with the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) call at logon.</span></span> <span data-ttu-id="159ed-118">このフラグNOTIFY_BEGIN_INBOUND設定すると、MAPI スプーラーは [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドへの呼び出しで渡された NOTIFY_NEWMAIL フラグを受け取る。</span><span class="sxs-lookup"><span data-stu-id="159ed-118">Once the NOTIFY_BEGIN_INBOUND flag is set, the MAPI spooler honors the NOTIFY_NEWMAIL flag passed in the call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method.</span></span> <span data-ttu-id="159ed-119">トランスポート プロバイダー セッションの状態テーブル行は [、IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出して返す前に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-119">The status table row for the transport provider session should be updated before returning by calling the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method.</span></span> <span data-ttu-id="159ed-120">このNOTIFY_BEGIN_INBOUNDとNOTIFY_END_INBOUNDは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="159ed-120">The NOTIFY_BEGIN_INBOUND and NOTIFY_END_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="159ed-121">NOTIFY_BEGIN_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="159ed-121">NOTIFY_BEGIN_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="159ed-122">トランスポート プロバイダーに対して、可能な限り迅速に受信メッセージを循環します。</span><span class="sxs-lookup"><span data-stu-id="159ed-122">Signals the transport provider to cycle through inbound messages as quickly as possible.</span></span> <span data-ttu-id="159ed-123">この通知に準拠するために、トランスポート プロバイダーは ModifyStatusRow を使用して、状態テーブル行の PR_STATUS_CODE ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの **STATUS_INBOUND_FLUSH** フラグをできるだけ早く設定する **必要** があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-123">To comply with this notification, the transport provider should set the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status table row as soon as it can, by using **ModifyStatusRow**.</span></span> <span data-ttu-id="159ed-124">受信メッセージング サイクルは、プロバイダーができるすべてのメッセージをダウンロードしたと判断した場合、または NOTIFY_END_INBOUND_FLUSH フラグが設定された **TransportNotify** メソッド呼び出しを受け取った場合に完了します。</span><span class="sxs-lookup"><span data-stu-id="159ed-124">An inbound messaging cycle is complete when the provider determines it has downloaded all it can, or when it has received a **TransportNotify** method call with the NOTIFY_END_INBOUND_FLUSH flag set.</span></span> <span data-ttu-id="159ed-125">受信メッセージング サイクルが終了するまで、プロバイダーは [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) メソッドを呼び出さなければ、受信メッセージの配信を高速化するためにオペレーティング システムにサイクルを拒否する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-125">Until the end of the inbound messaging cycle, the provider should not call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method or otherwise relinquish cycles to the operating system to speed delivery of incoming messages.</span></span> <span data-ttu-id="159ed-126">MAPI スプーラーは通常、クライアント アプリケーションを介してユーザーの要求に応じてのみ NOTIFY_BEGIN_INBOUND_FLUSH を使用してすべてのメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="159ed-126">This is acceptable because the MAPI spooler typically uses NOTIFY_BEGIN_INBOUND_FLUSH only in response to a user's request, via a client application, to deliver all messages now.</span></span> <span data-ttu-id="159ed-127">受信フラッシュ操作の最後に、プロバイダーは **SpoolerNotify** を使用して、状態行の PR_STATUS_CODE プロパティの **STATUS_INBOUND_FLUSH** フラグをクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-127">At the end of the inbound flush operation, the provider should use **SpoolerNotify** to clear the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** property of its status row.</span></span> 
    
<span data-ttu-id="159ed-128">NOTIFY_BEGIN_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="159ed-128">NOTIFY_BEGIN_OUTBOUND</span></span> 
  
> <span data-ttu-id="159ed-129">このトランスポート プロバイダー セッションで送信操作が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-129">Outbound operations can now occur for this transport provider session.</span></span> <span data-ttu-id="159ed-130">このプロバイダーに送信するメッセージがある場合は [、IXPLogon::SubmitMessage](ixplogon-submitmessage.md) メソッドの呼び出しが続きます。</span><span class="sxs-lookup"><span data-stu-id="159ed-130">If there are any messages to be sent for this provider, a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method follows.</span></span> <span data-ttu-id="159ed-131">このセッションの状態テーブル行は、戻る前に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-131">The status table row for this session should be updated before returning.</span></span> <span data-ttu-id="159ed-132">フラグNOTIFY_BEGIN_OUTBOUNDとNOTIFY_END_OUTBOUNDは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="159ed-132">The NOTIFY_BEGIN_OUTBOUND and NOTIFY_END_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="159ed-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="159ed-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="159ed-134">このフラグと同様NOTIFY_BEGIN_INBOUND_FLUSH動作しますが、送信メッセージを参照します。</span><span class="sxs-lookup"><span data-stu-id="159ed-134">Works similarly to the NOTIFY_BEGIN_INBOUND_FLUSH flag, but refers to outbound messages.</span></span> <span data-ttu-id="159ed-135">適切な状態フラグがSTATUS_OUTBOUND_FLUSH。</span><span class="sxs-lookup"><span data-stu-id="159ed-135">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
<span data-ttu-id="159ed-136">NOTIFY_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="159ed-136">NOTIFY_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="159ed-137">MAPI スプーラーは  _、lppvData_ パラメーターが **IXPLogon::SubmitMessage** メソッド呼び出しから 32 ビット値をポイントするメッセージの転送を取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-137">The MAPI spooler must cancel transfer of the message for which the  _lppvData_ parameter points to the 32-bit value from the **IXPLogon::SubmitMessage** method call.</span></span> <span data-ttu-id="159ed-138">メッセージに関連付けられている **SubmitMessage、IXPLogon::StartMessage、\*\*\*\*または IXPLogon::EndMessage** メソッド呼び出しから返されるトランスポート プロバイダーなしで、NOTIFY_CANCEL_MESSAGE フラグを設定できます。 </span><span class="sxs-lookup"><span data-stu-id="159ed-138">The NOTIFY_CANCEL_MESSAGE flag can be set without the transport provider having returned from the **SubmitMessage**, **IXPLogon::StartMessage**, or **IXPLogon::EndMessage** method call that is associated with the message.</span></span> <span data-ttu-id="159ed-139">トランスポート プロバイダーは、取り消されたメッセージを処理するエントリ ポイントからできるだけ早く返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-139">The transport provider must return as soon as possible from the entry point that is handling the canceled message.</span></span> <span data-ttu-id="159ed-140">現在処理されている受信メッセージの場合、トランスポート プロバイダーは受信メッセージが現在保存されている場所に保存し、次の便利な時刻にもう一度配信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-140">For an inbound message that is currently being processed, the transport provider should save the incoming message wherever it is presently stored and deliver it again at the next convenient time.</span></span> <span data-ttu-id="159ed-141">受信メッセージに対して既に格納されているメッセージ オブジェクト データは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="159ed-141">The message object data already stored for the incoming message is discarded.</span></span> <span data-ttu-id="159ed-142">トランスポート プロバイダーが **StartMessage** または **SubmitMessage** の時刻にこの 32 ビット値を更新しなかった場合、値は送信メッセージの場合は 0、受信メッセージの場合は 1 です。</span><span class="sxs-lookup"><span data-stu-id="159ed-142">If the transport provider did not update this 32-bit value at the **StartMessage** or **SubmitMessage** time, the value is 0 for outbound messages and 1 for inbound messages.</span></span> 
    
<span data-ttu-id="159ed-143">NOTIFY_END_INBOUND</span><span class="sxs-lookup"><span data-stu-id="159ed-143">NOTIFY_END_INBOUND</span></span> 
  
> <span data-ttu-id="159ed-144">受信操作は、このトランスポート プロバイダー セッションで停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-144">Inbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="159ed-145">MAPI スプーラーは Pollメソッドの使用を停止し、このセッションNOTIFY_NEWMAILを無視します。</span><span class="sxs-lookup"><span data-stu-id="159ed-145">The MAPI spooler ceases to use the **Poll** method and ignores NOTIFY_NEWMAIL for this session.</span></span> <span data-ttu-id="159ed-146">インプロセス メッセージは完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-146">In-process messages should be completed.</span></span> <span data-ttu-id="159ed-147">トランスポート セッションの状態テーブル行は [、ModifyStatusRow](imapisupport-modifystatusrow.md) を呼び出して更新してから戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-147">The status table row for the transport session should be updated by calling [ModifyStatusRow](imapisupport-modifystatusrow.md) before returning.</span></span> <span data-ttu-id="159ed-148">このNOTIFY_END_INBOUNDとNOTIFY_BEGIN_INBOUNDは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="159ed-148">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="159ed-149">NOTIFY_END_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="159ed-149">NOTIFY_END_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="159ed-150">受信フラッシュ モードから抜け出すトランスポート プロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="159ed-150">Notifies the transport provider to come out of inbound flush mode.</span></span> <span data-ttu-id="159ed-151">トランスポート プロバイダーはダウンロードを停止する必要がありますが、ダウンロードはバックグラウンドで行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-151">The transport provider should not stop downloading, but downloading should be done in the background.</span></span> <span data-ttu-id="159ed-152">トランスポート セッションの状態テーブル行は、トランスポート プロバイダーがこの通知に準拠できる場合に **ModifyStatusRow** を呼び出して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-152">The status table row for the transport session should be updated by calling **ModifyStatusRow** when the transport provider can comply with this notification.</span></span> 
    
<span data-ttu-id="159ed-153">NOTIFY_END_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="159ed-153">NOTIFY_END_OUTBOUND</span></span> 
  
> <span data-ttu-id="159ed-154">このトランスポート プロバイダー セッションでは、送信操作が停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-154">Outbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="159ed-155">MAPI スプーラーは **SubmitMessage** の呼び出しを停止し、スプー **ラーNotify フラグをNOTIFY_READYTOSEND** します。</span><span class="sxs-lookup"><span data-stu-id="159ed-155">The MAPI spooler ceases to call **SubmitMessage** and ignores the **SpoolerNotify** NOTIFY_READYTOSEND flag.</span></span> <span data-ttu-id="159ed-156">現在送信されている送信メッセージがある場合は、停止しない必要があります。メッセージの配信を停止するには、メッセージ フラグをNOTIFY_CANCEL_MESSAGEします。</span><span class="sxs-lookup"><span data-stu-id="159ed-156">If there is an outbound message currently being sent, it should not be stopped; to stop delivery of a message, use the NOTIFY_CANCEL_MESSAGE flag.</span></span> <span data-ttu-id="159ed-157">このセッションの状態テーブルの行は **、ModifyStatusRow** を呼び出して戻す前に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-157">The status table row for this session should be updated by calling **ModifyStatusRow** before returning.</span></span> <span data-ttu-id="159ed-158">フラグNOTIFY_END_INBOUNDとNOTIFY_BEGIN_OUTBOUNDは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="159ed-158">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="159ed-159">NOTIFY_END_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="159ed-159">NOTIFY_END_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="159ed-160">送信メッセージと同様NOTIFY_END_INBOUND_FLUSH動作しますが、送信メッセージを参照します。</span><span class="sxs-lookup"><span data-stu-id="159ed-160">Works similarly to NOTIFY_END_INBOUND_FLUSH, but refers to outbound messages.</span></span> <span data-ttu-id="159ed-161">適切な状態フラグがSTATUS_OUTBOUND_FLUSH。</span><span class="sxs-lookup"><span data-stu-id="159ed-161">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
 <span data-ttu-id="159ed-162">_lppvData_</span><span class="sxs-lookup"><span data-stu-id="159ed-162">_lppvData_</span></span>
  
> <span data-ttu-id="159ed-163">[out]イベント固有のデータへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="159ed-163">[out] A pointer to a pointer to event-specific data.</span></span> <span data-ttu-id="159ed-164">_lppvData が指定する内容の_ 詳細については _、lpulFlags パラメーターの説明を参照_ してください。</span><span class="sxs-lookup"><span data-stu-id="159ed-164">For more information about what  _lppvData_ specifies, see the description for the  _lpulFlags_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="159ed-165">戻り値</span><span class="sxs-lookup"><span data-stu-id="159ed-165">Return value</span></span>

<span data-ttu-id="159ed-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="159ed-166">S_OK</span></span> 
  
> <span data-ttu-id="159ed-167">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="159ed-167">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="159ed-168">注釈</span><span class="sxs-lookup"><span data-stu-id="159ed-168">Remarks</span></span>

<span data-ttu-id="159ed-169">MAPI スプーラーは **、IXPLogon::TransportNotify** メソッドを呼び出して、通知が要求されたイベントについてトランスポート プロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="159ed-169">The MAPI spooler calls the **IXPLogon::TransportNotify** method to signal the transport provider about events for which notification has been requested.</span></span> <span data-ttu-id="159ed-170">これらのイベントには、メッセージ転送をキャンセルする MAPI スプーラー要求、受信または送信トランスポート操作の開始または終了、および受信メッセージ キューまたは送信メッセージ キューをクリアする操作の開始または終了が含まれます。</span><span class="sxs-lookup"><span data-stu-id="159ed-170">These events include a MAPI spooler request to cancel a message transfer, the beginning or ending of inbound or outbound transport operations, and the beginning or ending of an operation to clear an inbound or outbound message queue.</span></span> 
  
<span data-ttu-id="159ed-171">ユーザーがトランスポート プロバイダーが以前に延期したメッセージを取り消そうとすると、MAPI スプーラーは **TransportNotify** を呼び出し  _、ulFlags_ の NOTIFY_ABORT_DEFERRED フラグと NOTIFY_CANCEL_MESSAGE フラグの両方を渡します。</span><span class="sxs-lookup"><span data-stu-id="159ed-171">When the user tries to cancel a message that the transport provider has previously deferred, the MAPI spooler calls **TransportNotify**, passing in both the NOTIFY_ABORT_DEFERRED and NOTIFY_CANCEL_MESSAGE flags in  _ulFlags_.</span></span> <span data-ttu-id="159ed-172">MAPI スプーラーがログオフ中でキューにメッセージが残っている場合は **、TransportNotify** を呼び出NOTIFY_ABORT_DEFERRED _ulFlags_ でのみメッセージを渡します。</span><span class="sxs-lookup"><span data-stu-id="159ed-172">If the MAPI spooler is logging off and still has messages in the queue, it passes only NOTIFY_ABORT_DEFERRED in  _ulFlags_ when it calls **TransportNotify**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="159ed-173">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="159ed-173">Notes to implementers</span></span>

<span data-ttu-id="159ed-174">MAPI スプーラーは別の実行スレッドから、または別のウィンドウのプロシージャからこのメソッドを呼び出すので、プロバイダーは、この呼び出しでデータへのアクセスを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="159ed-174">The provider must synchronize access to its data on this call, because the MAPI spooler can invoke this method from another thread of execution or from a procedure for a different window.</span></span> <span data-ttu-id="159ed-175">これは、ほとんどの場合、MAPI スプーラーがトランスポート プロバイダーが送信を開始したメッセージの取り消しを通知するときに発生します。</span><span class="sxs-lookup"><span data-stu-id="159ed-175">This will most likely occur when the MAPI spooler signals the cancellation of a message that the transport provider has started sending.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="159ed-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="159ed-176">See also</span></span>

- [<span data-ttu-id="159ed-177">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="159ed-177">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md) 
- [<span data-ttu-id="159ed-178">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="159ed-178">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md) 
- [<span data-ttu-id="159ed-179">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="159ed-179">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md) 
- [<span data-ttu-id="159ed-180">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="159ed-180">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md) 
- [<span data-ttu-id="159ed-181">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="159ed-181">IXPLogon::Poll</span></span>](ixplogon-poll.md)
- [<span data-ttu-id="159ed-182">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="159ed-182">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
- [<span data-ttu-id="159ed-183">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="159ed-183">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
- [<span data-ttu-id="159ed-184">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="159ed-184">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="159ed-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="159ed-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

