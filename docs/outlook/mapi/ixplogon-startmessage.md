---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3758cf72aa79dbf500138e96872352950fafbd2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801263"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="210d4-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="210d4-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="210d4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="210d4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="210d4-105">MAPI スプーラーをトランスポート プロバイダーからの受信メッセージの転送を開始します。</span><span class="sxs-lookup"><span data-stu-id="210d4-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="210d4-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="210d4-106">Parameters</span></span>

 <span data-ttu-id="210d4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="210d4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="210d4-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="210d4-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="210d4-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="210d4-109">_lpMessage_</span></span>
  
> <span data-ttu-id="210d4-110">[in]オブジェクトへのポインターをメッセージ (受信メッセージを表す) にアクセスしてそのメッセージを操作するトランスポート プロバイダーによって使用される、読み取り/書き込み権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="210d4-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="210d4-111">トランスポート プロバイダーは、 **IXPLogon::StartMessage**への呼び出しから制御が戻った後、このオブジェクトは有効期限のままになります。</span><span class="sxs-lookup"><span data-stu-id="210d4-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="210d4-112">_lpulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="210d4-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="210d4-113">[out]メッセージに割り当てられている参照の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="210d4-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="210d4-114">MAPI スプーラーは、トランスポート プロバイダーへのポインターを返す前に、1 にこの値を初期化します。</span><span class="sxs-lookup"><span data-stu-id="210d4-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="210d4-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="210d4-115">Return value</span></span>

<span data-ttu-id="210d4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="210d4-116">S_OK</span></span> 
  
> <span data-ttu-id="210d4-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="210d4-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="210d4-118">����</span><span class="sxs-lookup"><span data-stu-id="210d4-118">Remarks</span></span>

<span data-ttu-id="210d4-119">MAPI スプーラーは、MAPI スプーラーをトランスポート プロバイダーからの受信メッセージの転送を開始するのには**IXPLogon::StartMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="210d4-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="210d4-120">_LpMessage_が指すメッセージに使用するトランスポート プロバイダーが開始されると、前に[IXPLogon::TransportNotify](ixplogon-transportnotify.md)メソッドを呼び出すことで潜在的な使用に対応する_lpulMsgRef_パラメーターにメッセージの参照が格納される必要があります。</span><span class="sxs-lookup"><span data-stu-id="210d4-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="210d4-121">**StartMessage**の呼び出し中に MAPI スプーラーは、メッセージの転送中に開かれるオブジェクトのメソッドを処理しもすべての添付ファイルを処理します。</span><span class="sxs-lookup"><span data-stu-id="210d4-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="210d4-122">この処理時間がかかることができます。</span><span class="sxs-lookup"><span data-stu-id="210d4-122">This processing can take a long time.</span></span> <span data-ttu-id="210d4-123">トランスポート プロバイダーは、他のシステム タスクの CPU 時間を解放するには、この処理中に頻繁に、MAPI スプーラーの[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)コールバック関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="210d4-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="210d4-124">トランスポート プロバイダーを作成、メッセージの受信者テーブル内のすべての受信者には、必要なすべてのアドレス指定プロパティを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="210d4-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="210d4-125">必要に応じて、プロバイダーは、特定の受信者を表すためのカスタム受信者を作成できます。</span><span class="sxs-lookup"><span data-stu-id="210d4-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="210d4-126">ただし、プロバイダーが複数の情報が含まれる受信者のエントリを生成できる場合に行ってください。</span><span class="sxs-lookup"><span data-stu-id="210d4-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="210d4-127">など、トランスポート プロバイダーにその形式の受信者のエントリの有効な識別子を構築できます、アドレス帳プロバイダーの受信者の形式について十分な情報がある場合は、エントリの識別子を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="210d4-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="210d4-128">Nontransmittable プロパティは、受信した場合トランスポート プロバイダーは、保存しないようにして新しいメッセージにします。</span><span class="sxs-lookup"><span data-stu-id="210d4-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="210d4-129">ただし、トランスポート プロバイダーは、新しいメッセージを受信するすべての転送可能なプロパティを格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="210d4-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="210d4-130">着信メッセージが配信レポートまたは配信不能レポートには、トランスポート プロバイダーは、 [IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを使用して、元のメッセージからレポートを生成することは、プロバイダーする必要があります自体を先に設定のメッセージ適切なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="210d4-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="210d4-131">ただし、トランスポート プロバイダーは、メッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティを設定できません。</span><span class="sxs-lookup"><span data-stu-id="210d4-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="210d4-132">処理後、適切な MAPI メッセージ ・ ストアに受信メッセージを保存するには、トランスポート プロバイダーは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="210d4-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="210d4-133">トランスポート プロバイダーがすべてのメッセージを MAPI スプーラーを無効にするのには、 **SaveChanges**を呼び出すことがなく、 **StartMessage**の呼び出しから返すことで、着信メッセージを停止できます。</span><span class="sxs-lookup"><span data-stu-id="210d4-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="210d4-134">返す前に**StartMessage**の呼び出し中に、トランスポート プロバイダーが表示されるすべてのオブジェクトを解放するようにします。</span><span class="sxs-lookup"><span data-stu-id="210d4-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="210d4-135">ただし、プロバイダーでは、MAPI スプーラーが最初_lpMessage_パラメーターに渡されるメッセージ オブジェクトは開放しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="210d4-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="210d4-136">**StartMessage**がエラーを返した場合プロセス内のメッセージは変更内容を保存せずにリリースがされ、失われます。</span><span class="sxs-lookup"><span data-stu-id="210d4-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="210d4-137">この例では、トランスポート プロバイダーは[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出して、NOTIFY_CRITICAL_ERROR フラグを渡すし、MAPI スプーラーの重大なエラー状態であることを通知するために[IXPLogon::Poll](ixplogon-poll.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="210d4-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="210d4-138">詳細については、 [MAPI スプーラーと対話する](interacting-with-the-mapi-spooler.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="210d4-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="210d4-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="210d4-139">See also</span></span>



[<span data-ttu-id="210d4-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="210d4-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="210d4-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="210d4-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="210d4-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="210d4-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="210d4-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="210d4-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="210d4-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="210d4-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="210d4-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="210d4-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="210d4-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="210d4-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="210d4-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="210d4-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

