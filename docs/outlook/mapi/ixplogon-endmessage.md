---
title: IXPLogonEndMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.EndMessage
api_type:
- COM
ms.assetid: bb29e6a0-7a92-46eb-bbeb-6f2df6ac6d21
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f727d68e0e193e8f2e148d881968993f836f8ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582470"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="6e259-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="6e259-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="6e259-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e259-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e259-105">トランスポート プロバイダーは、MAPI スプーラーに送信メッセージの処理が完了したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="6e259-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6e259-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6e259-106">Parameters</span></span>

 <span data-ttu-id="6e259-107">_ulMsgRef_</span><span class="sxs-lookup"><span data-stu-id="6e259-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="6e259-108">[in][IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドへの以前の呼び出しで取得したメッセージに固有の参照値です。</span><span class="sxs-lookup"><span data-stu-id="6e259-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="6e259-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="6e259-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="6e259-110">[out]メッセージで行う必要があります、MAPI スプーラーを示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="6e259-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="6e259-111">フラグが設定されていない場合、メッセージは送信されました。</span><span class="sxs-lookup"><span data-stu-id="6e259-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="6e259-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6e259-112">The following flags can be set:</span></span>
    
<span data-ttu-id="6e259-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="6e259-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="6e259-114">トランスポート プロバイダーは、ここではこのメッセージが表示に必要なすべての情報を持ちます。</span><span class="sxs-lookup"><span data-stu-id="6e259-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="6e259-115">トランスポート プロバイダーは、詳細を必要とする場合、またはメッセージを送信したときは、NOTIFY_SENTDEFERRED フラグを指定して[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出すことによって、メッセージのエントリ id を渡すことによって、MAPI スプーラーを通知します。</span><span class="sxs-lookup"><span data-stu-id="6e259-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="6e259-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="6e259-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="6e259-117">トランスポート プロバイダーは、エラー条件ではないため現時点でのメッセージを送信しません。</span><span class="sxs-lookup"><span data-stu-id="6e259-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="6e259-118">トランスポート プロバイダーは、呼び出す必要がありますもう一度メッセージを送信するのには後でします。</span><span class="sxs-lookup"><span data-stu-id="6e259-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="6e259-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="6e259-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="6e259-120">トランスポート プロバイダーは、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドの呼び出しで渡されたメッセージを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e259-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6e259-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6e259-121">Return value</span></span>

<span data-ttu-id="6e259-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e259-122">S_OK</span></span> 
  
> <span data-ttu-id="6e259-123">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6e259-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e259-124">注釈</span><span class="sxs-lookup"><span data-stu-id="6e259-124">Remarks</span></span>

<span data-ttu-id="6e259-125">MAPI スプーラーは、拡張の配信または配信不能の情報を提供することに関連する処理が完了した後に、 **IXPLogon::EndMessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e259-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="6e259-126">この呼び出しが返されると、 _ulMsgRef_パラメーターの値はこのメッセージに対して有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="6e259-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="6e259-127">トランスポート プロバイダーは、今後のメッセージに同じ値を再利用できます。</span><span class="sxs-lookup"><span data-stu-id="6e259-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="6e259-128">MAPI スプーラーは、トランスポート プロバイダーに渡されるメッセージ オブジェクトを除いて、 **EndMessage**呼び出しが戻る前にトランスポート プロバイダーがメッセージの転送中に表示されるすべてのオブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e259-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="6e259-129">MAPI スプーラーによって渡されるメッセージ オブジェクトは、 **EndMessage**の呼び出しの後は有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="6e259-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e259-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e259-130">See also</span></span>



[<span data-ttu-id="6e259-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="6e259-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="6e259-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="6e259-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="6e259-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="6e259-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="6e259-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e259-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

