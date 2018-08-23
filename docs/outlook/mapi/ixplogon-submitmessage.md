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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 28e7874d1e61c0a4fe0ad702f206ca03a9a1096a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575876"
---
# <a name="ixplogonsubmitmessage"></a><span data-ttu-id="65868-103">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="65868-103">IXPLogon::SubmitMessage</span></span>

  
  
<span data-ttu-id="65868-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65868-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65868-105">MAPI スプーラーがメッセージを配信するトランスポート プロバイダーを持っていることを示します。</span><span class="sxs-lookup"><span data-stu-id="65868-105">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a><span data-ttu-id="65868-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="65868-106">Parameters</span></span>

 <span data-ttu-id="65868-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="65868-107">_ulFlags_</span></span>
  
> <span data-ttu-id="65868-108">[in]メッセージの送信方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="65868-108">[in] A bitmask of flags that controls how the message is submitted.</span></span> <span data-ttu-id="65868-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="65868-109">The following flag can be set:</span></span>
    
<span data-ttu-id="65868-110">BEGIN_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="65868-110">BEGIN_DEFERRED</span></span> 
  
> <span data-ttu-id="65868-111">MAPI スプーラーは既に遅延されたメッセージのトランスポート プロバイダーを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="65868-111">The MAPI spooler is calling a transport provider with a message that was previously deferred.</span></span> <span data-ttu-id="65868-112">メッセージのエントリ id は、それが延期された場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="65868-112">The entry identifier of the message is the same as when it was deferred.</span></span> <span data-ttu-id="65868-113">メッセージは、MAPI スプーラーを無効に NOTIFY_SENTDEFERRED フラグを指定して[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを使用して、そのエントリの識別子を渡すことによって延期されました。</span><span class="sxs-lookup"><span data-stu-id="65868-113">The message was deferred by passing its entry identifier back to the MAPI spooler by using the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag.</span></span> 
    
 <span data-ttu-id="65868-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="65868-114">_lpMessage_</span></span>
  
> <span data-ttu-id="65868-115">[in]トランスポート プロバイダーを使用してアクセスし、そのメッセージを操作する、読み取り/書き込み権限を持っている (配信されるメッセージを表す)、メッセージ オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="65868-115">[in] A pointer to a message object (representing the message to deliver) that has read/write permission, which the transport provider uses to access and manipulate that message.</span></span> <span data-ttu-id="65868-116">トランスポート プロバイダーは、 [IXPLogon::EndMessage](ixplogon-endmessage.md)メソッドへの後続の呼び出しから制御が戻った後、このオブジェクトは有効期限のままになります。</span><span class="sxs-lookup"><span data-stu-id="65868-116">This object remains valid until after the transport provider returns from a subsequent call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
    
 <span data-ttu-id="65868-117">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="65868-117">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="65868-118">[out]トランスポート プロバイダーがそれには、このメッセージに割り当てられている参照の値を返します。 変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="65868-118">[out] A pointer to a variable in which the transport provider returns the reference value it assigned to this message.</span></span> <span data-ttu-id="65868-119">MAPI スプーラーは、このメッセージの後続の呼び出しでこの参照値を渡します。</span><span class="sxs-lookup"><span data-stu-id="65868-119">The MAPI spooler passes this reference value in subsequent calls for this message.</span></span> <span data-ttu-id="65868-120">MAPI スプーラーは、トランスポート プロバイダーを返す前に 0 に値を初期化します。</span><span class="sxs-lookup"><span data-stu-id="65868-120">The MAPI spooler initializes the value to 0 before returning it to the transport provider.</span></span>
    
 <span data-ttu-id="65868-121">_lpulReturnParm_</span><span class="sxs-lookup"><span data-stu-id="65868-121">_lpulReturnParm_</span></span>
  
> <span data-ttu-id="65868-122">[out]**SubmitMessage**によって返される MAPI_E_WAIT または MAPI_E_NETWORK_ERROR のエラー値に対応する変数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="65868-122">[out] A pointer to a variable that corresponds to the MAPI_E_WAIT or MAPI_E_NETWORK_ERROR error value returned by **SubmitMessage**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65868-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="65868-123">Return value</span></span>

<span data-ttu-id="65868-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="65868-124">S_OK</span></span> 
  
> <span data-ttu-id="65868-125">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="65868-125">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="65868-126">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="65868-126">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="65868-127">トランスポート プロバイダーは、別の操作を実行しているために、メッセージを処理できません。</span><span class="sxs-lookup"><span data-stu-id="65868-127">The transport provider cannot handle the message, because it is performing another operation.</span></span> <span data-ttu-id="65868-128">プロバイダーでは、処理が発生していないことと、MAPI スプーラーが**EndMessage**を呼び出す必要がありますいないことを示すためにこの戻り値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-128">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span> <span data-ttu-id="65868-129">MAPI スプーラーは、 **SubmitMessage**の呼び出しを後で再試行されます。</span><span class="sxs-lookup"><span data-stu-id="65868-129">The MAPI spooler will try the **SubmitMessage** call again later.</span></span> 
    
<span data-ttu-id="65868-130">MAPI_E_CANCEL</span><span class="sxs-lookup"><span data-stu-id="65868-130">MAPI_E_CANCEL</span></span> 
  
> <span data-ttu-id="65868-131">トランスポート プロバイダーは、 **SpoolerNotify**呼び出しの前にメッセージを MAPI スプーラーが再送信を要求された条件が変更されたため、メッセージを再送しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-131">Although the transport provider requested that the MAPI spooler resubmit the message on a previous **SpoolerNotify** call, conditions have since changed, and the message should not be resent.</span></span> <span data-ttu-id="65868-132">MAPI スプーラーが他の何かの処理に進みます。</span><span class="sxs-lookup"><span data-stu-id="65868-132">The MAPI spooler will go on to handle something else.</span></span> 
    
<span data-ttu-id="65868-133">MAPI_E_NETWORK_ERROR</span><span class="sxs-lookup"><span data-stu-id="65868-133">MAPI_E_NETWORK_ERROR</span></span> 
  
> <span data-ttu-id="65868-134">ネットワーク エラーでは、操作が正常に完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="65868-134">A network error prevented successful completion of the operation.</span></span> <span data-ttu-id="65868-135">_LpulReturnParm_パラメーターは、MAPI スプーラーが、メッセージを再送信するまでの秒数を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-135">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
<span data-ttu-id="65868-136">MAPI_E_NOT_ME</span><span class="sxs-lookup"><span data-stu-id="65868-136">MAPI_E_NOT_ME</span></span> 
  
> <span data-ttu-id="65868-137">トランスポート プロバイダーは、このメッセージを処理できません。</span><span class="sxs-lookup"><span data-stu-id="65868-137">The transport provider cannot handle this message.</span></span> <span data-ttu-id="65868-138">別のトランスポート プロバイダーを検索するのには、MAPI スプーラーを無効してください。</span><span class="sxs-lookup"><span data-stu-id="65868-138">The MAPI spooler should try to find another transport provider for it.</span></span> <span data-ttu-id="65868-139">プロバイダーでは、処理が発生していないことと、MAPI スプーラーが**EndMessage**を呼び出す必要がありますいないことを示すためにこの戻り値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-139">A provider should use this return value to indicate that no processing occurred and that the MAPI spooler should not call **EndMessage**.</span></span>
    
<span data-ttu-id="65868-140">MAPI_E_WAIT</span><span class="sxs-lookup"><span data-stu-id="65868-140">MAPI_E_WAIT</span></span> 
  
> <span data-ttu-id="65868-141">一時的な問題では、トランスポート プロバイダーがメッセージを処理できなくなります。</span><span class="sxs-lookup"><span data-stu-id="65868-141">A temporary problem prevents the transport provider from handling the message.</span></span> <span data-ttu-id="65868-142">_LpulReturnParm_パラメーターは、MAPI スプーラーが、メッセージを再送信するまでの秒数を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-142">The  _lpulReturnParm_ parameter should be set to the number of seconds that will elapse before the MAPI spooler resubmits the message.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="65868-143">注釈</span><span class="sxs-lookup"><span data-stu-id="65868-143">Remarks</span></span>

<span data-ttu-id="65868-144">MAPI スプーラーは、必要があるメッセージを配信するトランスポート プロバイダーの場合、 **IXPLogon::SubmitMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="65868-144">The MAPI spooler calls the **IXPLogon::SubmitMessage** method when it has a message for the transport provider to deliver.</span></span> <span data-ttu-id="65868-145">メッセージは、 _lpMessage_パラメーターを使用して、トランスポート プロバイダーに渡されます。</span><span class="sxs-lookup"><span data-stu-id="65868-145">The message is passed to the transport provider by using the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="65868-146">プロバイダーがメッセージを受信する準備ができた場合は、 _lpulMsgRef_パラメーター、プロセス、渡されたオブジェクトを使用して参照値を返すし、適切な値 (通常は S_OK) を返すする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-146">If the provider is ready to accept the message, it should return a reference value by using the  _lpulMsgRef_ parameter, process the passed object, and return the appropriate value (usually S_OK).</span></span> <span data-ttu-id="65868-147">プロバイダーが転送を処理する準備ができていない場合は、エラー値を返す必要があり、必要に応じて、別の MAPI 戻り値でメッセージを再送信する前に、MAPI スプーラーが待機する時間の長さを示すために_lpulReturnParm_ 。</span><span class="sxs-lookup"><span data-stu-id="65868-147">If the provider is not prepared to handle the transfer, it should return an error value and, optionally, another MAPI return value in  _lpulReturnParm_ to indicate how long the MAPI spooler should wait before resubmitting the message.</span></span> 
  
<span data-ttu-id="65868-148">このメソッドの実装をトランスポート プロバイダーは、次に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="65868-148">A transport provider's implementation of this method can do the following:</span></span>
  
- <span data-ttu-id="65868-149">可能性のあるローカル ・ ストレージにメッセージをコピー、転送を待機する内部のキューにメッセージを配置しを返します。</span><span class="sxs-lookup"><span data-stu-id="65868-149">Put the message into an internal queue to wait for transmission, possibly copying the message to local storage, and return.</span></span>
    
- <span data-ttu-id="65868-150">実際の転送を実行し、転送が完了すると、正常終了または失敗のいずれかを取得しようとします。</span><span class="sxs-lookup"><span data-stu-id="65868-150">Attempt to perform the actual transmission and return when the transmission completes, either successfully or unsuccessfully.</span></span>
    
- <span data-ttu-id="65868-151">関連するリソースを確認した後にメッセージを送信するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="65868-151">Determine whether to send the message after checking the resource involved.</span></span> <span data-ttu-id="65868-152">この例では、リソースが空の場合は、プロバイダー リソースをロック、メッセージを準備して提出できること。</span><span class="sxs-lookup"><span data-stu-id="65868-152">In this case, if the resource is free, the provider can lock the resource, prepare the message, and submit it.</span></span> <span data-ttu-id="65868-153">リソースがビジー状態の場合は、プロバイダーはメッセージを準備し、後で送信を延期できます。</span><span class="sxs-lookup"><span data-stu-id="65868-153">If the resource is busy, the provider can prepare the message and defer sending to a later time.</span></span>
    
<span data-ttu-id="65868-154">メッセージの伝送のための手法をお勧めは、トランスポート プロバイダーやプロセスがシステム リソースの競合の数によって異なります。</span><span class="sxs-lookup"><span data-stu-id="65868-154">The preferred technique for message transmission depends on the transport provider and the expected number of processes competing for system resources.</span></span> 
  
<span data-ttu-id="65868-155">**SubmitMessage**の呼び出し中には、トランスポート プロバイダーは、メッセージ オブジェクトからのメッセージのデータの転送を制御します。</span><span class="sxs-lookup"><span data-stu-id="65868-155">During a **SubmitMessage** call, the transport provider controls the transfer of message data from the message object.</span></span> <span data-ttu-id="65868-156">ただし、トランスポート プロバイダーは、先にポインターを返します_lpulMsgRef_データを転送する前に、メッセージに参照値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-156">However, the transport provider should assign a reference value to the message, to which it returns a pointer in  _lpulMsgRef_, before transferring data.</span></span> <span data-ttu-id="65868-157">MAPI スプーラー プロセス中に任意の時点で NOTIFY_CANCEL_MESSAGE フラグを指定して[IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドを呼び出すことができますので設定ことを示すプロバイダーは任意の開いているオブジェクトを解放するメッセージの転送を停止します。</span><span class="sxs-lookup"><span data-stu-id="65868-157">It does so because at any point during the process, the MAPI spooler can call the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method with the NOTIFY_CANCEL_MESSAGE flag set to signal the provider that it should release any open objects and stop message transfer.</span></span> 
  
<span data-ttu-id="65868-158">トランスポート プロバイダーは、メッセージの任意の nontransmittable プロパティを送信することはできません。</span><span class="sxs-lookup"><span data-stu-id="65868-158">The transport provider should not send any nontransmittable properties of the message.</span></span> <span data-ttu-id="65868-159">このようなプロパティが検出されるに移動します、次のプロパティを処理します。</span><span class="sxs-lookup"><span data-stu-id="65868-159">When it finds such a property, it should go on to process the next property.</span></span> <span data-ttu-id="65868-160">プロバイダーは、送信されたメッセージのコンテンツの一部として MAPI_P1 の受信者情報を表示しないように、あらゆる努力をする必要があります。プロバイダーは、目的のアドレスに対してのみ、この受信者の情報を使用してください。</span><span class="sxs-lookup"><span data-stu-id="65868-160">The provider should make every effort not to display MAPI_P1 recipient information as part of the transmitted message content; the provider should use this recipient information only for addressing purposes.</span></span> <span data-ttu-id="65868-161">MAPI_P1 の受信者は、メッセージを再送信に使用される内部で生成された受信者です。それらは転送されませんする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-161">MAPI_P1 recipients are internally generated recipients that are used for resending messages; they should not be transmitted.</span></span> <span data-ttu-id="65868-162">代わりに、他の受信者を使用して、受信者情報を送信するためです。</span><span class="sxs-lookup"><span data-stu-id="65868-162">Instead, use the other recipients for transmitting recipient information.</span></span> <span data-ttu-id="65868-163">この方法の目的は、元の受信者として正確な同じ受信者テーブルを表示する受信者を再送信を許可するように。</span><span class="sxs-lookup"><span data-stu-id="65868-163">The purpose of this arrangement is to permit resend recipients to see the exact same recipient table as the original recipients.</span></span>
  
<span data-ttu-id="65868-164">**SubmitMessage**の呼び出し中に MAPI スプーラーは、メッセージの転送中に開かれているオブジェクトのメソッドを処理し、すべての添付ファイルを処理します。</span><span class="sxs-lookup"><span data-stu-id="65868-164">During a **SubmitMessage** call, the MAPI spooler processes methods for objects that are opened during the transfer of the message, and it processes any attachments.</span></span> <span data-ttu-id="65868-165">この処理時間がかかることができます。</span><span class="sxs-lookup"><span data-stu-id="65868-165">This processing can take a long time.</span></span> <span data-ttu-id="65868-166">トランスポート プロバイダーは、他のシステム タスクの CPU 時間を解放するには、この処理中に頻繁に、MAPI スプーラーの[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="65868-166">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="65868-167">すべてのメッセージ受信者は、MAPI スプーラーが最初に渡されるメッセージの受信者テーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="65868-167">All message recipients are visible in the recipient table of the message that the MAPI spooler originally passed.</span></span> <span data-ttu-id="65868-168">トランスポート プロバイダーに処理可能な受信者のみを処理する必要があります-エントリ id、アドレスの種類、またはその両方に基づいて-をしていない、**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを TRUE に設定するとします。</span><span class="sxs-lookup"><span data-stu-id="65868-168">The transport provider should process only those recipients that it can handle — based on entry identifier, address type, or both — and that do not already have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to TRUE.</span></span> <span data-ttu-id="65868-169">**れない**は既に TRUE に設定されている別のトランスポート プロバイダーがその受信者を処理します。</span><span class="sxs-lookup"><span data-stu-id="65868-169">If **PR_RESPONSIBILITY** is already set to TRUE, another transport provider has handled that recipient.</span></span> <span data-ttu-id="65868-170">プロバイダーには、その受信者にメッセージを処理できるかどうかを判断するのには受信者のための十分な処理が完了すると、その必要がありますその受信者の**れない**プロパティを設定、渡されたメッセージの場合は TRUE。</span><span class="sxs-lookup"><span data-stu-id="65868-170">When the provider completes sufficient processing of a recipient to determine whether it can handle messages for that recipient, it should set that recipient's **PR_RESPONSIBILITY** property to TRUE in the passed message.</span></span> <span data-ttu-id="65868-171">通常、メッセージの配信が完了した後、プロバイダーは、この決定により、です。</span><span class="sxs-lookup"><span data-stu-id="65868-171">Usually, the provider makes this determination after message delivery is complete.</span></span> 
  
<span data-ttu-id="65868-172">通常、トランスポート プロバイダーを返さない**SubmitMessage**の呼び出しからのメッセージ データの転送が完了するまでです。</span><span class="sxs-lookup"><span data-stu-id="65868-172">Typically, the transport provider does not return from a **SubmitMessage** call until it completes the transfer of message data.</span></span> <span data-ttu-id="65868-173">エラーが返されない場合プロバイダーに、MAPI スプーラーから次の呼び出しは、 [IXPLogon::EndMessage](ixplogon-endmessage.md)メソッドを呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="65868-173">If no error is returned, the next call from the MAPI spooler to the provider is a call to the [IXPLogon::EndMessage](ixplogon-endmessage.md) method.</span></span> 
  
<span data-ttu-id="65868-174">**SubmitMessage**がエラーを返した場合、MAPI スプーラーは変更を保存せずプロセス内のメッセージを解放します。</span><span class="sxs-lookup"><span data-stu-id="65868-174">If **SubmitMessage** returns an error, the MAPI spooler releases the message in process without saving changes.</span></span> <span data-ttu-id="65868-175">トランスポート プロバイダーでは、メッセージの変更を保存する必要がある場合は、戻る前にメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すする必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-175">If the transport provider requires message changes to be saved, it must call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the message before returning.</span></span> 
  
<span data-ttu-id="65868-176">トランスポートの問題が原因で発生するエラーが発生した場合、MAPI スプーラーが、メッセージを保持ですが、 _lpulReturnParm_で返される値に基づいてトランスポート プロバイダーは、メッセージを再送信することなきます。</span><span class="sxs-lookup"><span data-stu-id="65868-176">In case of errors that occur because of transport problems, the MAPI spooler retains the message, but it delays resubmitting the message to the transport provider based on the value returned in  _lpulReturnParm_.</span></span> <span data-ttu-id="65868-177">トランスポート プロバイダーはする必要があります**SubmitMessage**からの戻り値の値が MAPI_E_WAIT または MAPI_E_NETWORK_ERROR である場合に、その値を入力します。</span><span class="sxs-lookup"><span data-stu-id="65868-177">The transport provider must fill in that value if its return value from **SubmitMessage** is MAPI_E_WAIT or MAPI_E_NETWORK_ERROR.</span></span> <span data-ttu-id="65868-178">重大なエラー状態が発生した場合、トランスポート プロバイダーは、NOTIFY_CRITICAL_ERROR フラグを指定して[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="65868-178">If a severe error condition occurs, the transport provider must call the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_CRITICAL_ERROR flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65868-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="65868-179">See also</span></span>



[<span data-ttu-id="65868-180">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="65868-180">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="65868-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="65868-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="65868-182">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="65868-182">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="65868-183">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="65868-183">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="65868-184">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="65868-184">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="65868-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65868-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

