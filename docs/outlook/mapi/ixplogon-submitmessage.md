---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ae124cb94cff5be0a655386d31f1bf2c82f66a85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423322"
---
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="e8440-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e8440-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="e8440-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8440-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8440-105">MAPI スプーラーにトランスポート プロバイダーが配信するメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e8440-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="e8440-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8440-106">Parameters</span></span>

 <span data-ttu-id="e8440-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e8440-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e8440-108">[in]メッセージの送信方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e8440-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="e8440-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e8440-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e8440-110">BEGIN_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="e8440-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="e8440-111">MAPI スプーラーは、以前に延期されたメッセージを含むトランスポート プロバイダーを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="e8440-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="e8440-112">メッセージのエントリ識別子は、延期された場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="e8440-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="e8440-113">メッセージは [、IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドを NOTIFY_SENTDEFERRED フラグと一緒に使用して、MAPI スプーラーにエントリ識別子を渡して延期されました。</span><span class="sxs-lookup"><span data-stu-id="e8440-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="e8440-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e8440-114">_lpMessage_</span></span>
  
> <span data-ttu-id="e8440-115">[in]読み取り/書き込みアクセス許可を持つメッセージ オブジェクト (配信するメッセージを表す) へのポインター。トランスポート プロバイダーは、そのメッセージにアクセスして操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="e8440-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="e8440-116">このオブジェクトは、トランスポート プロバイダーが [IXPLogon::EndMessage](ixplogon-endmessage.md) メソッドへの後続の呼び出しから戻るまで有効です。</span><span class="sxs-lookup"><span data-stu-id="e8440-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="e8440-117">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="e8440-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="e8440-118">[out]トランスポート プロバイダーが、このメッセージに割り当てられた参照値を返す変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8440-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="e8440-119">MAPI スプーラーは、このメッセージの後続の呼び出しでこの参照値を渡します。</span><span class="sxs-lookup"><span data-stu-id="e8440-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="e8440-120">MAPI スプーラーは、トランスポート プロバイダーに返す前に値を 0 に初期化します。</span><span class="sxs-lookup"><span data-stu-id="e8440-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="e8440-121">_lpulReturnParm_</span><span class="sxs-lookup"><span data-stu-id="e8440-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="e8440-122">[out] **SubmitMessage** によって返されるエラー値またはエラー値に対応MAPI_E_WAIT変数MAPI_E_NETWORK_ERRORポインターです。</span><span class="sxs-lookup"><span data-stu-id="e8440-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8440-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="e8440-123">Return value</span></span>

<span data-ttu-id="e8440-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8440-124">S_OK</span></span> 
  
> <span data-ttu-id="e8440-125">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="e8440-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="e8440-126">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e8440-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e8440-127">トランスポート プロバイダーは、別の操作を実行するために、メッセージを処理できません。</span><span class="sxs-lookup"><span data-stu-id="e8440-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="e8440-128">プロバイダーは、この戻り値を使用して、処理が発生し、MAPI スプーラーが EndMessage を呼び出す必要がないかどうかを **示す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="e8440-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="e8440-129">MAPI スプーラーは、後で **SubmitMessage 呼び出しを** 再試行します。</span><span class="sxs-lookup"><span data-stu-id="e8440-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="e8440-130">MAPI_E_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e8440-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="e8440-131">トランスポート プロバイダーは、MAPI スプーラーが以前のスプーラー **Notify** 呼び出しでメッセージを再送信することを要求したが、その後、条件が変更され、メッセージを再送信する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e8440-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="e8440-132">MAPI スプーラーは、他の処理に進むでしょう。</span><span class="sxs-lookup"><span data-stu-id="e8440-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="e8440-133">MAPI_E_NETWORK_ERROR</span><span class="sxs-lookup"><span data-stu-id="e8440-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="e8440-134">ネットワーク エラーによって、操作が正常に完了しなかった。</span><span class="sxs-lookup"><span data-stu-id="e8440-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="e8440-135">_lpulReturnParm_ パラメーターは、MAPI スプーラーがメッセージを再送信するまでに経過する秒の数に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="e8440-136">MAPI_E_NOT_ME</span><span class="sxs-lookup"><span data-stu-id="e8440-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="e8440-137">トランスポート プロバイダーは、このメッセージを処理できません。</span><span class="sxs-lookup"><span data-stu-id="e8440-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="e8440-138">MAPI スプーラーは、別のトランスポート プロバイダーを検索しようとする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="e8440-139">プロバイダーは、この戻り値を使用して、処理が発生し、MAPI スプーラーが EndMessage を呼び出す必要がないかどうかを **示す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="e8440-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="e8440-140">MAPI_E_WAIT</span><span class="sxs-lookup"><span data-stu-id="e8440-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="e8440-141">一時的な問題により、トランスポート プロバイダーはメッセージを処理しきれな。</span><span class="sxs-lookup"><span data-stu-id="e8440-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="e8440-142">_lpulReturnParm_ パラメーターは、MAPI スプーラーがメッセージを再送信するまでに経過する秒の数に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e8440-143">注釈</span><span class="sxs-lookup"><span data-stu-id="e8440-143">Remarks</span></span>

<span data-ttu-id="e8440-144">MAPI スプーラーは、トランスポート プロバイダーが配信するメッセージがある場合に **IXPLogon::SubmitMessage** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e8440-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="e8440-145">メッセージは、lpMessage パラメーターを使用してトランスポート  _プロバイダーに渡_ されます。</span><span class="sxs-lookup"><span data-stu-id="e8440-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="e8440-146">プロバイダーがメッセージを受け入れる準備ができている場合は  _、lpulMsgRef_ パラメーターを使用して参照値を返し、渡されたオブジェクトを処理し、適切な値 (通常は S_OK) を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="e8440-147">プロバイダーが転送を処理する準備がされていない場合は、エラー値を返し、必要に応じて  _lpulReturnParm_ の別の MAPI 戻り値を返して、MAPI スプーラーがメッセージを再送信するまでに待機する時間を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="e8440-148">トランスポート プロバイダーによるこのメソッドの実装では、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="e8440-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="e8440-149">メッセージを内部キューに入れて、転送を待ち、メッセージをローカル ストレージにコピーして戻す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="e8440-150">実際の送信を実行し、正常または失敗した場合に送信が完了した場合に返します。</span><span class="sxs-lookup"><span data-stu-id="e8440-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="e8440-151">関係するリソースを確認した後でメッセージを送信するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e8440-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="e8440-152">この場合、リソースが空きである場合、プロバイダーはリソースをロックし、メッセージを準備し、送信できます。</span><span class="sxs-lookup"><span data-stu-id="e8440-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="e8440-153">リソースがビジー状態の場合、プロバイダーはメッセージを準備し、後で送信を延期できます。</span><span class="sxs-lookup"><span data-stu-id="e8440-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="e8440-154">メッセージ送信の推奨手法は、トランスポート プロバイダーと、システム リソースと競合する予想されるプロセス数によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e8440-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="e8440-155">**SubmitMessage 呼び出し** 中に、トランスポート プロバイダーはメッセージ オブジェクトからのメッセージ データの転送を制御します。</span><span class="sxs-lookup"><span data-stu-id="e8440-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="e8440-156">ただし、トランスポート プロバイダーは、データを転送する前に  _、lpulMsgRef_ でポインターを返すメッセージに参照値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="e8440-157">この処理は、プロセス中の任意の時点で、MAPI スプーラーが NOTIFY_CANCEL_MESSAGE フラグを設定して [IXPLogon::TransportNotify](ixplogon-transportnotify.md) メソッドを呼び出して、開いているオブジェクトを解放し、メッセージ転送を停止する必要があるというメッセージをプロバイダーに知らされる可能性があるからです。</span><span class="sxs-lookup"><span data-stu-id="e8440-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="e8440-158">トランスポート プロバイダーは、メッセージの非送信可能なプロパティを送信できません。</span><span class="sxs-lookup"><span data-stu-id="e8440-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="e8440-159">そのようなプロパティを見つけたら、次のプロパティを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="e8440-160">プロバイダーは、送信されたメッセージコンテンツの一部としてMAPI_P1情報を表示しなくあらゆる努力をする必要があります。プロバイダーは、この受信者情報をアドレス指定の目的でのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="e8440-161">MAPI_P1受信者は、メッセージの再送信に使用される内部的に生成された受信者です。送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="e8440-162">代わりに、他の受信者を使用して受信者情報を送信します。</span><span class="sxs-lookup"><span data-stu-id="e8440-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="e8440-163">この配置の目的は、受信者が元の受信者とまったく同じ受信者テーブルを再送信して表示を許可する目的です。</span><span class="sxs-lookup"><span data-stu-id="e8440-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="e8440-164">**SubmitMessage 呼び出** し中に、MAPI スプーラーはメッセージの転送中に開いたオブジェクトのメソッドを処理し、添付ファイルを処理します。</span><span class="sxs-lookup"><span data-stu-id="e8440-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="e8440-165">この処理には長い時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-165">This processing can take a long time.</span></span> <span data-ttu-id="e8440-166">トランスポート プロバイダーは、この処理中に MAPI スプーラーの [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) メソッドを頻繁に呼び出して、他のシステム タスクの CPU 時間を解放できます。</span><span class="sxs-lookup"><span data-stu-id="e8440-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="e8440-167">すべてのメッセージ受信者は、MAPI スプーラーが最初に渡したメッセージの受信者テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e8440-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="e8440-168">トランスポート プロバイダーは、エントリ識別子、アドレスの種類、または両方に基づいて処理できる受信者のみを処理し **、PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティが TRUE に設定されていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="e8440-169">既 **PR_RESPONSIBILITY** TRUE に設定されている場合、別のトランスポート プロバイダーが受信者を処理しました。</span><span class="sxs-lookup"><span data-stu-id="e8440-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="e8440-170">プロバイダーが受信者のメッセージを処理できるかどうかを判断するために十分な処理が完了したら、渡されたメッセージで受信者の **PR_RESPONSIBILITY** プロパティを TRUE に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="e8440-171">通常、プロバイダーはメッセージ配信が完了した後でこの決定を行います。</span><span class="sxs-lookup"><span data-stu-id="e8440-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="e8440-172">通常、トランスポート プロバイダーは、メッセージ データの転送が完了するまで **SubmitMessage** 呼び出しから返されません。</span><span class="sxs-lookup"><span data-stu-id="e8440-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="e8440-173">エラーが返されない場合、MAPI スプーラーからプロバイダーへの次の呼び出しは [、IXPLogon::EndMessage](ixplogon-endmessage.md) メソッドへの呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="e8440-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="e8440-174">**SubmitMessage が** エラーを返す場合、MAPI スプーラーは変更を保存せずにメッセージを処理中に解放します。</span><span class="sxs-lookup"><span data-stu-id="e8440-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="e8440-175">トランスポート プロバイダーがメッセージの変更を保存する必要がある場合は、返す前にメッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="e8440-176">トランスポートの問題が原因でエラーが発生した場合、MAPI スプーラーはメッセージを保持しますが  _、lpulReturnParm_ で返される値に基づいてトランスポート プロバイダーへのメッセージの再送信が遅延します。</span><span class="sxs-lookup"><span data-stu-id="e8440-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="e8440-177">**SubmitMessage** からの戻り値が指定されている場合、トランスポート プロバイダーは、その値を入力MAPI_E_WAITまたはMAPI_E_NETWORK_ERROR。</span><span class="sxs-lookup"><span data-stu-id="e8440-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="e8440-178">重大なエラー状態が発生した場合、トランスポート プロバイダーは [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドを呼び出し、NOTIFY_CRITICAL_ERRORする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8440-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8440-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8440-179">See also</span></span>



[<span data-ttu-id="e8440-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e8440-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="e8440-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="e8440-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="e8440-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="e8440-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="e8440-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="e8440-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="e8440-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="e8440-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="e8440-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8440-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

