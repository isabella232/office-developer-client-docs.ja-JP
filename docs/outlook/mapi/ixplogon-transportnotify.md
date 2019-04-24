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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351563"
---
# <a name="ixplogontransportnotify"></a><span data-ttu-id="92d3b-103">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="92d3b-103">IXPLogon::TransportNotify</span></span>

<span data-ttu-id="92d3b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92d3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92d3b-105">トランスポートプロバイダーが通知を要求したイベントが発生したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-105">Signals the occurrence of an event about which the transport provider requested notification.</span></span>
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a><span data-ttu-id="92d3b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92d3b-106">Parameters</span></span>

 <span data-ttu-id="92d3b-107">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="92d3b-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="92d3b-108">[入力]通知イベントを通知するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="92d3b-108">[in, out] A bitmask of flags that signals notification events.</span></span> <span data-ttu-id="92d3b-109">次のフラグは、入力時に MAPI スプーラーで設定でき、出力時に変更されずに返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-109">The following flags can be set by the MAPI spooler on input and must be returned unchanged on output:</span></span>
    
<span data-ttu-id="92d3b-110">NOTIFY_ABORT_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="92d3b-110">NOTIFY_ABORT_DEFERRED</span></span> 
  
> <span data-ttu-id="92d3b-111">役割が承認されたメッセージが延期されていることをトランスポートプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-111">Notifies the transport provider that a message for which it accepted responsibility is being deferred.</span></span> <span data-ttu-id="92d3b-112">遅延をサポートするトランスポートプロバイダーのみがこのフラグをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-112">Only transport providers that support deferral must support this flag.</span></span> <span data-ttu-id="92d3b-113">_lppvData_パラメーターは、取り消されたメッセージのエントリ識別子を指します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-113">The  _lppvData_ parameter points to the entry identifier of the canceled message.</span></span> <span data-ttu-id="92d3b-114">MAPI スプーラーで処理されていないメッセージは、 [IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)メソッドを呼び出して延期することができます。</span><span class="sxs-lookup"><span data-stu-id="92d3b-114">Messages that the MAPI spooler has not processed can still be deferred by calling the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method.</span></span> 
    
<span data-ttu-id="92d3b-115">NOTIFY_BEGIN_INBOUND</span><span class="sxs-lookup"><span data-stu-id="92d3b-115">NOTIFY_BEGIN_INBOUND</span></span> 
  
> <span data-ttu-id="92d3b-116">MAPI スプーラーは、このトランスポートプロバイダーセッションの受信メッセージを受け付けることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="92d3b-116">The MAPI spooler can now accept inbound messages for this transport provider session.</span></span> <span data-ttu-id="92d3b-117">MAPI スプーラーは、 [IXPLogon::P oll](ixplogon-poll.md)メソッドを定期的に呼び出します。トランスポートプロバイダーが、ログオン時に[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)呼び出しで LOGON_SP_POLL フラグを設定している場合。</span><span class="sxs-lookup"><span data-stu-id="92d3b-117">The MAPI spooler regularly calls the [IXPLogon::Poll](ixplogon-poll.md) method if the transport provider set the LOGON_SP_POLL flag with the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) call at logon.</span></span> <span data-ttu-id="92d3b-118">NOTIFY_BEGIN_INBOUND フラグが設定されると、MAPI スプーラーは[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドの呼び出しで渡される NOTIFY_NEWMAIL フラグを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="92d3b-118">Once the NOTIFY_BEGIN_INBOUND flag is set, the MAPI spooler honors the NOTIFY_NEWMAIL flag passed in the call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method.</span></span> <span data-ttu-id="92d3b-119">トランスポートプロバイダーセッションの状態テーブル行は、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを呼び出すことによって戻る前に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-119">The status table row for the transport provider session should be updated before returning by calling the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method.</span></span> <span data-ttu-id="92d3b-120">NOTIFY_BEGIN_INBOUND および NOTIFY_END_INBOUND フラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="92d3b-120">The NOTIFY_BEGIN_INBOUND and NOTIFY_END_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="92d3b-121">NOTIFY_BEGIN_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="92d3b-121">NOTIFY_BEGIN_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="92d3b-122">受信メッセージをできるだけ早くサイクル処理するようにトランスポートプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-122">Signals the transport provider to cycle through inbound messages as quickly as possible.</span></span> <span data-ttu-id="92d3b-123">この通知に準拠するには、トランスポートプロバイダーは、 **modifystatusrow**を使用して、状態テーブル行の**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの STATUS_INBOUND_FLUSH フラグをすぐに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-123">To comply with this notification, the transport provider should set the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status table row as soon as it can, by using **ModifyStatusRow**.</span></span> <span data-ttu-id="92d3b-124">受信メッセージングサイクルは、プロバイダーがすべてのダウンロード可能なものと判断した場合、または NOTIFY_END_INBOUND_FLUSH フラグが設定された**transportnotify**メソッド呼び出しを受信した場合に完了します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-124">An inbound messaging cycle is complete when the provider determines it has downloaded all it can, or when it has received a **TransportNotify** method call with the NOTIFY_END_INBOUND_FLUSH flag set.</span></span> <span data-ttu-id="92d3b-125">受信メッセージングサイクルが終了するまで、受信メッセージの配信を高速化するために、プロバイダーは[imapisupport:: SpoolerYield](imapisupport-spooleryield.md)メソッドを呼び出し、または、それ以外の方法でオペレーティングシステムに解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-125">Until the end of the inbound messaging cycle, the provider should not call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method or otherwise relinquish cycles to the operating system to speed delivery of incoming messages.</span></span> <span data-ttu-id="92d3b-126">通常、MAPI スプーラーは、クライアントアプリケーションを介してすべてのメッセージを配信するために、ユーザーの要求に対する応答としてのみ NOTIFY_BEGIN_INBOUND_FLUSH を使用するため、これは許容できるものになります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-126">This is acceptable because the MAPI spooler typically uses NOTIFY_BEGIN_INBOUND_FLUSH only in response to a user's request, via a client application, to deliver all messages now.</span></span> <span data-ttu-id="92d3b-127">着信フラッシュ操作の最後に、プロバイダーは**SpoolerNotify**を使用して、そのステータス行の**PR_STATUS_CODE**プロパティの STATUS_INBOUND_FLUSH フラグをクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-127">At the end of the inbound flush operation, the provider should use **SpoolerNotify** to clear the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** property of its status row.</span></span> 
    
<span data-ttu-id="92d3b-128">NOTIFY_BEGIN_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="92d3b-128">NOTIFY_BEGIN_OUTBOUND</span></span> 
  
> <span data-ttu-id="92d3b-129">このトランスポートプロバイダーセッションでは、送信操作が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-129">Outbound operations can now occur for this transport provider session.</span></span> <span data-ttu-id="92d3b-130">このプロバイダーに対して送信されるメッセージがある場合、 [IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッドの呼び出しは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-130">If there are any messages to be sent for this provider, a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method follows.</span></span> <span data-ttu-id="92d3b-131">このセッションの状態テーブル行は、戻る前に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-131">The status table row for this session should be updated before returning.</span></span> <span data-ttu-id="92d3b-132">NOTIFY_BEGIN_OUTBOUND および NOTIFY_END_OUTBOUND フラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="92d3b-132">The NOTIFY_BEGIN_OUTBOUND and NOTIFY_END_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="92d3b-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="92d3b-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="92d3b-134">NOTIFY_BEGIN_INBOUND_FLUSH フラグと同じように動作しますが、送信メッセージを参照します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-134">Works similarly to the NOTIFY_BEGIN_INBOUND_FLUSH flag, but refers to outbound messages.</span></span> <span data-ttu-id="92d3b-135">適切な状態フラグは STATUS_OUTBOUND_FLUSH です。</span><span class="sxs-lookup"><span data-stu-id="92d3b-135">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
<span data-ttu-id="92d3b-136">NOTIFY_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="92d3b-136">NOTIFY_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="92d3b-137">MAPI スプーラーは、 _lppvData_パラメーターが**IXPLogon:: submitmessage**メソッド呼び出しからの32ビット値をポイントするメッセージの転送をキャンセルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-137">The MAPI spooler must cancel transfer of the message for which the  _lppvData_ parameter points to the 32-bit value from the **IXPLogon::SubmitMessage** method call.</span></span> <span data-ttu-id="92d3b-138">NOTIFY_CANCEL_MESSAGE フラグは、メッセージに関連付けられている**submitmessage**、 **IXPLogon::: startmessage**、または**IXPLogon:: endmessage**メソッド呼び出しから返されたトランスポートプロバイダーを使用せずに設定できます。</span><span class="sxs-lookup"><span data-stu-id="92d3b-138">The NOTIFY_CANCEL_MESSAGE flag can be set without the transport provider having returned from the **SubmitMessage**, **IXPLogon::StartMessage**, or **IXPLogon::EndMessage** method call that is associated with the message.</span></span> <span data-ttu-id="92d3b-139">トランスポートプロバイダーは、取り消されたメッセージを処理するエントリポイントから、できるだけ早く戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-139">The transport provider must return as soon as possible from the entry point that is handling the canceled message.</span></span> <span data-ttu-id="92d3b-140">現在処理中の受信メッセージの場合、トランスポートプロバイダーは、受信メッセージを現在格納されている場所に保存し、次に都合のよい時間に再配信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-140">For an inbound message that is currently being processed, the transport provider should save the incoming message wherever it is presently stored and deliver it again at the next convenient time.</span></span> <span data-ttu-id="92d3b-141">受信メッセージ用に既に格納されているメッセージオブジェクトデータは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="92d3b-141">The message object data already stored for the incoming message is discarded.</span></span> <span data-ttu-id="92d3b-142">トランスポートプロバイダーが**startmessage**または**submitmessage**の時間でこの32ビット値を更新しなかった場合、送信メッセージの値は0で、受信メッセージの場合は1になります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-142">If the transport provider did not update this 32-bit value at the **StartMessage** or **SubmitMessage** time, the value is 0 for outbound messages and 1 for inbound messages.</span></span> 
    
<span data-ttu-id="92d3b-143">NOTIFY_END_INBOUND</span><span class="sxs-lookup"><span data-stu-id="92d3b-143">NOTIFY_END_INBOUND</span></span> 
  
> <span data-ttu-id="92d3b-144">このトランスポートプロバイダーセッションでは、受信操作を停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-144">Inbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="92d3b-145">MAPI スプーラーは、 **Poll**メソッドの使用を中止し、このセッションの NOTIFY_NEWMAIL を無視します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-145">The MAPI spooler ceases to use the **Poll** method and ignores NOTIFY_NEWMAIL for this session.</span></span> <span data-ttu-id="92d3b-146">インプロセスメッセージは完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-146">In-process messages should be completed.</span></span> <span data-ttu-id="92d3b-147">トランスポートセッションの状態テーブル行は、戻る前に[modifystatusrow](imapisupport-modifystatusrow.md)を呼び出して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-147">The status table row for the transport session should be updated by calling [ModifyStatusRow](imapisupport-modifystatusrow.md) before returning.</span></span> <span data-ttu-id="92d3b-148">NOTIFY_END_INBOUND および NOTIFY_BEGIN_INBOUND フラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="92d3b-148">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="92d3b-149">NOTIFY_END_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="92d3b-149">NOTIFY_END_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="92d3b-150">トランスポートプロバイダーに、着信フラッシュモードから出ていくことを通知します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-150">Notifies the transport provider to come out of inbound flush mode.</span></span> <span data-ttu-id="92d3b-151">トランスポートプロバイダーはダウンロードを停止する必要はありませんが、ダウンロードはバックグラウンドで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-151">The transport provider should not stop downloading, but downloading should be done in the background.</span></span> <span data-ttu-id="92d3b-152">トランスポートプロバイダーがこの通知に準拠できる場合は、[状態\*\*\*\* テーブルの行を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-152">The status table row for the transport session should be updated by calling **ModifyStatusRow** when the transport provider can comply with this notification.</span></span> 
    
<span data-ttu-id="92d3b-153">NOTIFY_END_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="92d3b-153">NOTIFY_END_OUTBOUND</span></span> 
  
> <span data-ttu-id="92d3b-154">このトランスポートプロバイダセッションに対して送信操作を停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-154">Outbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="92d3b-155">MAPI スプーラーは、 **submitmessage**の呼び出しを中止し、 **SpoolerNotify** NOTIFY_READYTOSEND フラグを無視します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-155">The MAPI spooler ceases to call **SubmitMessage** and ignores the **SpoolerNotify** NOTIFY_READYTOSEND flag.</span></span> <span data-ttu-id="92d3b-156">現在送信中の送信メッセージがある場合は、停止しないでください。メッセージの配信を停止するには、NOTIFY_CANCEL_MESSAGE フラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-156">If there is an outbound message currently being sent, it should not be stopped; to stop delivery of a message, use the NOTIFY_CANCEL_MESSAGE flag.</span></span> <span data-ttu-id="92d3b-157">このセッションの状態テーブル行は、戻る前に**modifystatusrow**を呼び出して更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-157">The status table row for this session should be updated by calling **ModifyStatusRow** before returning.</span></span> <span data-ttu-id="92d3b-158">NOTIFY_END_INBOUND および NOTIFY_BEGIN_OUTBOUND フラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="92d3b-158">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="92d3b-159">NOTIFY_END_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="92d3b-159">NOTIFY_END_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="92d3b-160">NOTIFY_END_INBOUND_FLUSH と同様に動作しますが、送信メッセージを参照します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-160">Works similarly to NOTIFY_END_INBOUND_FLUSH, but refers to outbound messages.</span></span> <span data-ttu-id="92d3b-161">適切な状態フラグは STATUS_OUTBOUND_FLUSH です。</span><span class="sxs-lookup"><span data-stu-id="92d3b-161">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
 <span data-ttu-id="92d3b-162">_lppvData_</span><span class="sxs-lookup"><span data-stu-id="92d3b-162">_lppvData_</span></span>
  
> <span data-ttu-id="92d3b-163">読み上げイベント固有のデータへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="92d3b-163">[out] A pointer to a pointer to event-specific data.</span></span> <span data-ttu-id="92d3b-164">_lppvData_で指定される内容の詳細については、 _l flags_パラメーターの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92d3b-164">For more information about what  _lppvData_ specifies, see the description for the  _lpulFlags_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="92d3b-165">戻り値</span><span class="sxs-lookup"><span data-stu-id="92d3b-165">Return value</span></span>

<span data-ttu-id="92d3b-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="92d3b-166">S_OK</span></span> 
  
> <span data-ttu-id="92d3b-167">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="92d3b-167">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92d3b-168">解説</span><span class="sxs-lookup"><span data-stu-id="92d3b-168">Remarks</span></span>

<span data-ttu-id="92d3b-169">MAPI スプーラーは**IXPLogon:: transportnotify**メソッドを呼び出して、通知が要求されたイベントについてトランスポートプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-169">The MAPI spooler calls the **IXPLogon::TransportNotify** method to signal the transport provider about events for which notification has been requested.</span></span> <span data-ttu-id="92d3b-170">これらのイベントには、メッセージ転送をキャンセルするための MAPI スプーラー要求、受信または送信トランスポート操作の開始または終了、および受信または送信メッセージキューをクリアする操作の開始または終了が含まれます。</span><span class="sxs-lookup"><span data-stu-id="92d3b-170">These events include a MAPI spooler request to cancel a message transfer, the beginning or ending of inbound or outbound transport operations, and the beginning or ending of an operation to clear an inbound or outbound message queue.</span></span> 
  
<span data-ttu-id="92d3b-171">トランスポートプロバイダーが以前に遅延していたメッセージをユーザーが取り消しようとすると、MAPI スプーラーは、NOTIFY_ABORT_DEFERRED と NOTIFY_CANCEL_MESSAGE の両方のフラグを_ulflags_に渡して、 **transportnotify**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-171">When the user tries to cancel a message that the transport provider has previously deferred, the MAPI spooler calls **TransportNotify**, passing in both the NOTIFY_ABORT_DEFERRED and NOTIFY_CANCEL_MESSAGE flags in  _ulFlags_.</span></span> <span data-ttu-id="92d3b-172">MAPI スプーラーがログオフしていてもキューにメッセージがある場合、NOTIFY_ABORT_DEFERRED は、 **transportnotify**を呼び出したときに_ulflags_にのみ渡されます。</span><span class="sxs-lookup"><span data-stu-id="92d3b-172">If the MAPI spooler is logging off and still has messages in the queue, it passes only NOTIFY_ABORT_DEFERRED in  _ulFlags_ when it calls **TransportNotify**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="92d3b-173">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="92d3b-173">Notes to implementers</span></span>

<span data-ttu-id="92d3b-174">MAPI スプーラーは別の実行スレッドから、または別のウィンドウのプロシージャからこのメソッドを呼び出すことができるため、プロバイダーはこの呼び出しでデータへのアクセスを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92d3b-174">The provider must synchronize access to its data on this call, because the MAPI spooler can invoke this method from another thread of execution or from a procedure for a different window.</span></span> <span data-ttu-id="92d3b-175">これは、通常、トランスポートプロバイダーが送信を開始したメッセージの取り消しを MAPI スプーラーが通知するときに発生します。</span><span class="sxs-lookup"><span data-stu-id="92d3b-175">This will most likely occur when the MAPI spooler signals the cancellation of a message that the transport provider has started sending.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="92d3b-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="92d3b-176">See also</span></span>

- [<span data-ttu-id="92d3b-177">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="92d3b-177">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md) 
- [<span data-ttu-id="92d3b-178">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="92d3b-178">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md) 
- [<span data-ttu-id="92d3b-179">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="92d3b-179">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md) 
- [<span data-ttu-id="92d3b-180">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="92d3b-180">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md) 
- [<span data-ttu-id="92d3b-181">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="92d3b-181">IXPLogon::Poll</span></span>](ixplogon-poll.md)
- [<span data-ttu-id="92d3b-182">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="92d3b-182">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
- [<span data-ttu-id="92d3b-183">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="92d3b-183">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
- [<span data-ttu-id="92d3b-184">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="92d3b-184">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="92d3b-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92d3b-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

