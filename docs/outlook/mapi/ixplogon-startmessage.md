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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427606"
---
# <a name="ixplogonstartmessage"></a><span data-ttu-id="d2b5a-103">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="d2b5a-103">IXPLogon::StartMessage</span></span>

  
  
<span data-ttu-id="d2b5a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2b5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2b5a-105">トランスポートプロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-105">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a><span data-ttu-id="d2b5a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d2b5a-106">Parameters</span></span>

 <span data-ttu-id="d2b5a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2b5a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d2b5a-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="d2b5a-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d2b5a-109">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="d2b5a-109">_lpMessage_</span></span>
  
> <span data-ttu-id="d2b5a-110">順番読み取り/書き込みアクセス許可を持つメッセージオブジェクト (受信メッセージを表す) へのポインター。これは、そのメッセージにアクセスして操作するためにトランスポートプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-110">[in] A pointer to a message object (representing the inbound message) that has read/write permission, which is used by the transport provider to access and manipulate that message.</span></span> <span data-ttu-id="d2b5a-111">このオブジェクトは、トランスポートプロバイダーが**IXPLogon:: startmessage**の呼び出しから戻るまで有効です。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-111">This object remains valid until after the transport provider returns from the call to **IXPLogon::StartMessage**.</span></span>
    
 <span data-ttu-id="d2b5a-112">_lアウト msグリーン f_</span><span class="sxs-lookup"><span data-stu-id="d2b5a-112">_lpulMsgRef_</span></span>
  
> <span data-ttu-id="d2b5a-113">読み上げメッセージに割り当てられている参照値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-113">[out] A pointer to a reference value assigned to the message.</span></span> <span data-ttu-id="d2b5a-114">MAPI スプーラーは、この値を1に初期化してから、トランスポートプロバイダーへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-114">The MAPI spooler initializes this value to 1 before it returns the pointer to the transport provider.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2b5a-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="d2b5a-115">Return value</span></span>

<span data-ttu-id="d2b5a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2b5a-116">S_OK</span></span> 
  
> <span data-ttu-id="d2b5a-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="d2b5a-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2b5a-118">注釈</span><span class="sxs-lookup"><span data-stu-id="d2b5a-118">Remarks</span></span>

<span data-ttu-id="d2b5a-119">mapi スプーラーは**IXPLogon:: startmessage**メソッドを呼び出して、トランスポートプロバイダーから mapi スプーラーへの受信メッセージの転送を開始します。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-119">The MAPI spooler calls the **IXPLogon::StartMessage** method to initiate the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span> <span data-ttu-id="d2b5a-120">_lpmessage_によって示されたメッセージの使用をトランスポートプロバイダーが開始する前に、 [IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッドの呼び出しによって使用される可能性のある_lアウト msグリーン f_パラメーターにメッセージ参照を格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-120">Before the transport provider starts to use the message pointed to by  _lpMessage_, it should store a message reference in the  _lpulMsgRef_ parameter for potential use by a call to the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method.</span></span> 
  
<span data-ttu-id="d2b5a-121">**startmessage**呼び出しの間、MAPI スプーラーは、メッセージの転送中に開かれたオブジェクトのメソッドを処理し、添付ファイルも処理します。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-121">During a **StartMessage** call, the MAPI spooler processes methods for objects opened during the transfer of the message, and it also processes any attachments.</span></span> <span data-ttu-id="d2b5a-122">この処理には長い時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-122">This processing can take a long time.</span></span> <span data-ttu-id="d2b5a-123">トランスポートプロバイダーは、この処理中に多くの場合、MAPI スプーラーの[imapisupport:: SpoolerYield](imapisupport-spooleryield.md) callback 関数を呼び出して、他のシステムタスクに対する CPU 時間を解放することができます。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-123">Transport providers can call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) callback function for the MAPI spooler frequently during this processing to release CPU time for other system tasks.</span></span> 
  
<span data-ttu-id="d2b5a-124">トランスポートプロバイダーがメッセージに対して作成する受信者テーブル内のすべての受信者に、必要なすべてのアドレス指定プロパティが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-124">All recipients in the recipient table that the transport provider creates for the message must contain all required addressing properties.</span></span> <span data-ttu-id="d2b5a-125">必要に応じて、プロバイダーは特定の受信者を表すカスタム受信者を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-125">If necessary, the provider can construct a custom recipient to represent a particular recipient.</span></span> <span data-ttu-id="d2b5a-126">ただし、プロバイダーが詳細情報を含む受信者エントリを作成できる場合は、そのようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-126">However, if the provider can produce a recipient entry that includes more information, it should do so.</span></span> <span data-ttu-id="d2b5a-127">たとえば、アドレス帳プロバイダーの受信者の形式に関する十分な情報がトランスポートプロバイダーにある場合、その形式の受信者に対して有効なエントリ識別子を作成することができます。そのためには、エントリ識別子を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-127">For example, if a transport provider has enough information about an address book provider's recipient format that it can build a valid entry identifier for a recipient for that format, it should build the entry identifier.</span></span>
  
<span data-ttu-id="d2b5a-128">転送不能なテーブルプロパティが受信されていない場合、トランスポートプロバイダーはそれらを新しいメッセージに格納することはできません。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-128">If any nontransmittable properties are received, the transport provider should not store them in the new message.</span></span> <span data-ttu-id="d2b5a-129">ただし、トランスポートプロバイダーは、新しいメッセージで受信するすべてのトランスポートテーブルプロパティを格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-129">However, the transport provider should store all transmittable properties it receives in the new message.</span></span>
  
<span data-ttu-id="d2b5a-130">受信メッセージが配信レポートまたは配信不能レポートで、トランスポートプロバイダーが[imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを使用して元のメッセージからレポートを生成できない場合は、プロバイダー自体に、次のようにメッセージを設定する必要があります。適切なプロパティ。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-130">If the incoming message is a delivery report or a nondelivery report and the transport provider is unable to use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to generate the report from the original message, the provider should itself populate the message with the appropriate properties.</span></span> <span data-ttu-id="d2b5a-131">ただし、トランスポートプロバイダーは、メッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを設定できません。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-131">However, the transport provider cannot set the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d2b5a-132">受信メッセージを適切な MAPI メッセージストアに処理した後に保存するには、トランスポートプロバイダーは[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-132">To save the incoming message in the appropriate MAPI message store after processing, the transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="d2b5a-133">トランスポートプロバイダーが MAPI スプーラーに渡すメッセージを持っていない場合は、 **SaveChanges**を呼び出さずに**startmessage**呼び出しから戻って、受信メッセージを停止することができます。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-133">If the transport provider does not have any messages to pass to the MAPI spooler, it can stop the incoming message by returning from the **StartMessage** call without calling **SaveChanges**.</span></span>
  
<span data-ttu-id="d2b5a-134">**startmessage**呼び出し中にトランスポートプロバイダが開くすべてのオブジェクトは、戻る前に解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-134">All objects that the transport provider opens during a **StartMessage** call should be released before returning.</span></span> <span data-ttu-id="d2b5a-135">ただし、プロバイダーは、MAPI スプーラーが最初に_lpmessage_パラメーターで渡したメッセージオブジェクトを解放することはできません。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-135">However, the provider should not release the message object that the MAPI spooler originally passed in the  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="d2b5a-136">**startmessage**がエラーを返した場合は、変更が保存されていない状態で処理中のメッセージが解放され、失われます。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-136">If **StartMessage** returns an error, the message in process is released without having changes saved and is lost.</span></span> <span data-ttu-id="d2b5a-137">この場合、トランスポートプロバイダーは、NOTIFY_CRITICAL_ERROR フラグを[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドの呼び出しと共に渡し、 [IXPLogon::P oll](ixplogon-poll.md)メソッドを呼び出して、重大なエラー状態にあることを MAPI スプーラーに通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-137">In this case, the transport provider should pass the NOTIFY_CRITICAL_ERROR flag with a call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method and call the [IXPLogon::Poll](ixplogon-poll.md) method to notify the MAPI spooler that it is in a severe error condition.</span></span> 
  
<span data-ttu-id="d2b5a-138">詳細については、「 [MAPI スプーラーとの対話](interacting-with-the-mapi-spooler.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2b5a-138">For more information, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2b5a-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2b5a-139">See also</span></span>



[<span data-ttu-id="d2b5a-140">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d2b5a-140">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="d2b5a-141">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="d2b5a-141">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="d2b5a-142">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="d2b5a-142">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="d2b5a-143">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="d2b5a-143">IMAPISupport::StatusRecips</span></span>](imapisupport-statusrecips.md)
  
[<span data-ttu-id="d2b5a-144">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="d2b5a-144">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="d2b5a-145">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="d2b5a-145">IXPLogon::Poll</span></span>](ixplogon-poll.md)
  
[<span data-ttu-id="d2b5a-146">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="d2b5a-146">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md)
  
[<span data-ttu-id="d2b5a-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2b5a-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

