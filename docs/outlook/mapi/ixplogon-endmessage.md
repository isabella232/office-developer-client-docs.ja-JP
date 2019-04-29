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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 03eccfe27c6f93e42ee01a34fbf5df766c145cf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414159"
---
# <a name="ixplogonendmessage"></a><span data-ttu-id="c2ec2-103">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="c2ec2-103">IXPLogon::EndMessage</span></span>

  
  
<span data-ttu-id="c2ec2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2ec2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2ec2-105">MAPI スプーラーが送信メッセージの処理を完了したことをトランスポートプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-105">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>
  
```cpp
HRESULT EndMessage(
  ULONG ulMsgRef,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c2ec2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c2ec2-106">Parameters</span></span>

 <span data-ttu-id="c2ec2-107">_ulmsグリーン f_</span><span class="sxs-lookup"><span data-stu-id="c2ec2-107">_ulMsgRef_</span></span>
  
> <span data-ttu-id="c2ec2-108">順番[IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッドを以前に呼び出したときに取得されたメッセージ固有の参照値。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-108">[in] A message-specific reference value that was obtained in an earlier call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> 
    
 <span data-ttu-id="c2ec2-109">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="c2ec2-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="c2ec2-110">読み上げメッセージに対して行うべきことを MAPI スプーラーに示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-110">[out] A bitmask of flags that indicates to the MAPI spooler what it should do with the message.</span></span> <span data-ttu-id="c2ec2-111">フラグが設定されていない場合は、メッセージが送信されています。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-111">If no flags are set, the message has been sent.</span></span> <span data-ttu-id="c2ec2-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-112">The following flags can be set:</span></span>
    
<span data-ttu-id="c2ec2-113">END_DONT_RESEND</span><span class="sxs-lookup"><span data-stu-id="c2ec2-113">END_DONT_RESEND</span></span> 
  
> <span data-ttu-id="c2ec2-114">この時点で、トランスポートプロバイダーには、このメッセージに関する必要な情報がすべて含まれています。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-114">The transport provider has all the information it needs about this message for now.</span></span> <span data-ttu-id="c2ec2-115">トランスポートプロバイダーがより多くの情報を必要とする場合や、メッセージを送信した場合は、NOTIFY_SENTDEFERRED フラグを使用して[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出し、メッセージのエントリ識別子を渡すことによって、MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-115">When the transport provider requires more information or when it has sent the message, it notifies the MAPI spooler by calling the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method with the NOTIFY_SENTDEFERRED flag and by passing the message's entry identifier.</span></span> 
    
<span data-ttu-id="c2ec2-116">END_RESEND_LATER</span><span class="sxs-lookup"><span data-stu-id="c2ec2-116">END_RESEND_LATER</span></span> 
  
> <span data-ttu-id="c2ec2-117">エラー状態ではない理由により、トランスポートプロバイダーが現時点でメッセージを送信していません。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-117">The transport provider is not sending the message at the current time for reasons that are not error conditions.</span></span> <span data-ttu-id="c2ec2-118">メッセージを送信するには、後でトランスポートプロバイダーを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-118">The transport provider should be called again later to send the message.</span></span>
    
<span data-ttu-id="c2ec2-119">END_RESEND_NOW</span><span class="sxs-lookup"><span data-stu-id="c2ec2-119">END_RESEND_NOW</span></span> 
  
> <span data-ttu-id="c2ec2-120">トランスポートプロバイダーは、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッド呼び出しで渡されたメッセージを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-120">The transport provider needs to restart the message passed to it in an [IMessage::SubmitMessage](imessage-submitmessage.md) method call.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c2ec2-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="c2ec2-121">Return value</span></span>

<span data-ttu-id="c2ec2-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2ec2-122">S_OK</span></span> 
  
> <span data-ttu-id="c2ec2-123">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-123">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2ec2-124">注釈</span><span class="sxs-lookup"><span data-stu-id="c2ec2-124">Remarks</span></span>

<span data-ttu-id="c2ec2-125">MAPI スプーラーは、拡張配信または配信不能情報の提供に関係する処理を完了した後、 **IXPLogon:: endmessage**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-125">The MAPI spooler calls the **IXPLogon::EndMessage** method after it completes the processing involved in providing extended delivery or nondelivery information.</span></span> 
  
<span data-ttu-id="c2ec2-126">この呼び出しが戻ると、このメッセージの_ulmsグリーン f_パラメーターの値は無効になります。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-126">Once this call returns, the value in the  _ulMsgRef_ parameter is no longer valid for this message.</span></span> <span data-ttu-id="c2ec2-127">トランスポートプロバイダーは、今後のメッセージで同じ値を再利用できます。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-127">The transport provider can reuse the same value on a future message.</span></span> 
  
<span data-ttu-id="c2ec2-128">メッセージの転送中にトランスポートプロバイダが開くすべてのオブジェクトは、 **endmessage**呼び出しが戻る前に解放される必要があります。これは、MAPI スプーラーがトランスポートプロバイダーに渡すメッセージオブジェクトを除きます。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-128">All objects that the transport provider opens during the transfer of a message should be released before the **EndMessage** call returns, with the exception of the message object that the MAPI spooler passes to the transport provider.</span></span> <span data-ttu-id="c2ec2-129">**endmessage**呼び出しの後、MAPI スプーラーによって渡されるメッセージオブジェクトは無効です。</span><span class="sxs-lookup"><span data-stu-id="c2ec2-129">The message object passed by the MAPI spooler is invalid after the **EndMessage** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2ec2-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2ec2-130">See also</span></span>



[<span data-ttu-id="c2ec2-131">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="c2ec2-131">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="c2ec2-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c2ec2-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="c2ec2-133">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c2ec2-133">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="c2ec2-134">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2ec2-134">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

