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
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="06f53-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="06f53-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="06f53-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06f53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06f53-105">トランスポートプロバイダーが配信するメッセージを MAPI スプーラーに指定します。</span><span class="sxs-lookup"><span data-stu-id="06f53-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="06f53-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="06f53-106">Parameters</span></span>

 <span data-ttu-id="06f53-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="06f53-107">_ulFlags_</span></span>
  
> <span data-ttu-id="06f53-108">順番メッセージの送信方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="06f53-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="06f53-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="06f53-109">The following flag can be set:</span></span>
    
<span data-ttu-id="06f53-110">BEGIN_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="06f53-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="06f53-111">MAPI スプーラーは、以前に延期されたメッセージでトランスポートプロバイダーを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="06f53-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="06f53-112">メッセージのエントリ識別子は、延期されたときと同じです。</span><span class="sxs-lookup"><span data-stu-id="06f53-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="06f53-113">NOTIFY_SENTDEFERRED フラグを使用して[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを使用することにより、メッセージはエントリ id を MAPI スプーラーに戻すことによって延期されました。</span><span class="sxs-lookup"><span data-stu-id="06f53-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="06f53-114">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="06f53-114">_lpMessage_</span></span>
  
> <span data-ttu-id="06f53-115">順番読み取り/書き込みアクセス許可を持つメッセージオブジェクト (配信するメッセージを表す) へのポインター。これは、トランスポートプロバイダーがそのメッセージにアクセスして操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="06f53-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="06f53-116">このオブジェクトは、トランスポートプロバイダーが[IXPLogon:: endmessage](ixplogon-endmessage.md)メソッドの次の呼び出しから戻るまで有効です。</span><span class="sxs-lookup"><span data-stu-id="06f53-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="06f53-117">_lアウト msグリーン f_</span><span class="sxs-lookup"><span data-stu-id="06f53-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="06f53-118">読み上げトランスポートプロバイダーが、このメッセージに割り当てた参照値を返す変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="06f53-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="06f53-119">MAPI スプーラーは、このメッセージに対する以降の呼び出しでこの参照値を渡します。</span><span class="sxs-lookup"><span data-stu-id="06f53-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="06f53-120">MAPI スプーラーは値を0に初期化してから、トランスポートプロバイダーに返します。</span><span class="sxs-lookup"><span data-stu-id="06f53-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="06f53-121">_lpulReturnParm_</span><span class="sxs-lookup"><span data-stu-id="06f53-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="06f53-122">読み上げ**submitmessage**によって返される MAPI_E_WAIT または MAPI_E_NETWORK_ERROR ERROR の値に対応する変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="06f53-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06f53-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="06f53-123">Return value</span></span>

<span data-ttu-id="06f53-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="06f53-124">S_OK</span></span> 
  
> <span data-ttu-id="06f53-125">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="06f53-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="06f53-126">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="06f53-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="06f53-127">トランスポートプロバイダーが別の操作を実行しているため、メッセージを処理できません。</span><span class="sxs-lookup"><span data-stu-id="06f53-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="06f53-128">プロバイダーは、この戻り値を使用して、処理が発生していないこと、および MAPI スプーラーが**endmessage**を呼び出すことができないことを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="06f53-129">MAPI スプーラーは、後で**submitmessage**呼び出しを再試行します。</span><span class="sxs-lookup"><span data-stu-id="06f53-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="06f53-130">MAPI_E_CANCEL</span><span class="sxs-lookup"><span data-stu-id="06f53-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="06f53-131">トランスポートプロバイダーは、MAPI スプーラーが以前の**SpoolerNotify**呼び出しでメッセージを再送信することを要求しましたが、条件は変更されたため、メッセージを再送信しないでください。</span><span class="sxs-lookup"><span data-stu-id="06f53-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="06f53-132">MAPI スプーラーは、別のものを処理するためにに進みます。</span><span class="sxs-lookup"><span data-stu-id="06f53-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="06f53-133">MAPI_E_NETWORK_ERROR</span><span class="sxs-lookup"><span data-stu-id="06f53-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="06f53-134">ネットワークエラーにより、操作が正常に完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="06f53-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="06f53-135">_lpulReturnParm_パラメーターは、MAPI スプーラーでメッセージが再送信されるまでの経過時間 (秒数) に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="06f53-136">MAPI_E_NOT_ME</span><span class="sxs-lookup"><span data-stu-id="06f53-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="06f53-137">トランスポートプロバイダーは、このメッセージを処理できません。</span><span class="sxs-lookup"><span data-stu-id="06f53-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="06f53-138">MAPI スプーラーは、別のトランスポートプロバイダーの検索を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="06f53-139">プロバイダーは、この戻り値を使用して、処理が発生していないこと、および MAPI スプーラーが**endmessage**を呼び出すことができないことを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="06f53-140">MAPI_E_WAIT</span><span class="sxs-lookup"><span data-stu-id="06f53-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="06f53-141">一時的な問題により、トランスポートプロバイダーがメッセージを処理できなくなります。</span><span class="sxs-lookup"><span data-stu-id="06f53-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="06f53-142">_lpulReturnParm_パラメーターは、MAPI スプーラーでメッセージが再送信されるまでの経過時間 (秒数) に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="06f53-143">注釈</span><span class="sxs-lookup"><span data-stu-id="06f53-143">Remarks</span></span>

<span data-ttu-id="06f53-144">MAPI スプーラーは、トランスポートプロバイダーが配信するメッセージを持っているときに、 **IXPLogon:: submitmessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="06f53-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="06f53-145">メッセージは、 _lpmessage_パラメーターを使用してトランスポートプロバイダーに渡されます。</span><span class="sxs-lookup"><span data-stu-id="06f53-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="06f53-146">プロバイダーがメッセージを受け入れる準備ができている場合は、 _lアウト msグリーン f_パラメーターを使用して参照値を返し、渡されたオブジェクトを処理して、適切な値 (通常は S_OK) を返します。</span><span class="sxs-lookup"><span data-stu-id="06f53-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="06f53-147">プロバイダーが転送を処理する準備ができていない場合は、エラー値を返し、必要に応じて、 _lpulReturnParm_の別の mapi の戻り値を返して、メッセージを再送信するまでに mapi スプーラーが待機する時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="06f53-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="06f53-148">このメソッドのトランスポートプロバイダーの実装では、次のことを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="06f53-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="06f53-149">メッセージを内部キューに配置して、送信を待機します。場合によっては、メッセージをローカルストレージにコピーして、を返します。</span><span class="sxs-lookup"><span data-stu-id="06f53-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="06f53-150">実際の送信を実行し、送信が完了したときに、成功または失敗のどちらかを試行します。</span><span class="sxs-lookup"><span data-stu-id="06f53-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="06f53-151">リソースを確認した後、メッセージを送信するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="06f53-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="06f53-152">この例では、リソースが空いている場合、プロバイダーはリソースをロックし、メッセージを準備して送信できます。</span><span class="sxs-lookup"><span data-stu-id="06f53-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="06f53-153">リソースがビジー状態である場合、プロバイダーはメッセージを準備し、後で送信を延期することができます。</span><span class="sxs-lookup"><span data-stu-id="06f53-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="06f53-154">メッセージ転送に推奨される方法は、トランスポートプロバイダーと、システムリソースに対して競合する予期されるプロセス数によって異なります。</span><span class="sxs-lookup"><span data-stu-id="06f53-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="06f53-155">**submitmessage**呼び出しの間、トランスポートプロバイダーは、message オブジェクトからのメッセージデータの転送を制御します。</span><span class="sxs-lookup"><span data-stu-id="06f53-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="06f53-156">ただし、トランスポートプロバイダーは、データを転送する前に、 _lアウト msグリーン f_でポインターを返す参照値をメッセージに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="06f53-157">そのためには、処理中の任意の時点で MAPI スプーラーは[IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッドを NOTIFY_CANCEL_MESSAGE flag セットで呼び出して、開いているオブジェクトを解放し、メッセージ転送を停止する必要があることをプロバイダーに通知することができます。</span><span class="sxs-lookup"><span data-stu-id="06f53-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="06f53-158">トランスポートプロバイダーは、メッセージの転送不能なテーブルプロパティを送信することはできません。</span><span class="sxs-lookup"><span data-stu-id="06f53-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="06f53-159">そのようなプロパティが見つかったら、次のプロパティを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="06f53-160">プロバイダーは、送信されたメッセージコンテンツの一部として MAPI_P1 受信者情報を表示しないように、すべての努力を行う必要があります。プロバイダーは、アドレス指定のためにのみこの受信者情報を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="06f53-161">MAPI_P1 の受信者は、メッセージの再送信に使用される内部で生成された受信者です。送信されないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="06f53-162">代わりに、他の受信者を使用して受信者情報を送信します。</span><span class="sxs-lookup"><span data-stu-id="06f53-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="06f53-163">この方法の目的は、再送者が元の受信者とまったく同じ受信者テーブルを表示することを許可することです。</span><span class="sxs-lookup"><span data-stu-id="06f53-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="06f53-164">**submitmessage**呼び出しの間、MAPI スプーラーは、メッセージの転送中に開かれるオブジェクトのメソッドを処理し、添付ファイルを処理します。</span><span class="sxs-lookup"><span data-stu-id="06f53-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="06f53-165">この処理には長い時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="06f53-165">This processing can take a long time.</span></span> <span data-ttu-id="06f53-166">トランスポートプロバイダーは、この処理中に多くの場合、MAPI スプーラーの[imapisupport:: SpoolerYield](imapisupport-spooleryield.md)メソッドを呼び出して、他のシステムタスクの CPU 時間を解放できます。</span><span class="sxs-lookup"><span data-stu-id="06f53-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="06f53-167">すべてのメッセージの受信者は、MAPI スプーラーが最初に渡されたメッセージの recipient テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="06f53-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="06f53-168">トランスポートプロバイダーは、エントリ識別子、アドレスの種類、またはその両方に基づいて処理できる受信者のみを処理する必要があります。また、 **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティが TRUE に設定されていません。</span><span class="sxs-lookup"><span data-stu-id="06f53-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="06f53-169">**PR_RESPONSIBILITY**が既に TRUE に設定されている場合、別のトランスポートプロバイダーがその受信者を処理しています。</span><span class="sxs-lookup"><span data-stu-id="06f53-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="06f53-170">受信者が受信者のメッセージを処理できるかどうかを判断するために、プロバイダーがその受信者の十分な処理を完了した場合、渡されたメッセージの受信者の**PR_RESPONSIBILITY**プロパティを TRUE に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="06f53-171">通常、メッセージの配信が完了した後、プロバイダーはこの判断を行います。</span><span class="sxs-lookup"><span data-stu-id="06f53-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="06f53-172">通常、トランスポートプロバイダーは、メッセージデータの転送が完了するまで、 **submitmessage**呼び出しからは戻りません。</span><span class="sxs-lookup"><span data-stu-id="06f53-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="06f53-173">エラーが返されない場合、MAPI スプーラーからプロバイダーへの次の呼び出しは、 [IXPLogon:: endmessage](ixplogon-endmessage.md)メソッドの呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="06f53-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="06f53-174">**submitmessage**がエラーを返した場合、MAPI スプーラーは変更を保存せずに、処理中のメッセージを解放します。</span><span class="sxs-lookup"><span data-stu-id="06f53-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="06f53-175">トランスポートプロバイダーがメッセージの変更を保存する必要がある場合は、返す前にメッセージに対して[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="06f53-176">トランスポートの問題が原因でエラーが発生した場合、MAPI スプーラーはそのメッセージを保持しますが、 _lpulReturnParm_で返された値に基づいてトランスポートプロバイダーへのメッセージの送信を遅らせます。</span><span class="sxs-lookup"><span data-stu-id="06f53-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="06f53-177">**submitmessage**からの戻り値が MAPI_E_WAIT または MAPI_E_NETWORK_ERROR の場合、トランスポートプロバイダーはその値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="06f53-178">重大なエラー状態が発生した場合、トランスポートプロバイダーは、NOTIFY_CRITICAL_ERROR フラグを使用して[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f53-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06f53-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="06f53-179">See also</span></span>



[<span data-ttu-id="06f53-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="06f53-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="06f53-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="06f53-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="06f53-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="06f53-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="06f53-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="06f53-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="06f53-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="06f53-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="06f53-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06f53-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

