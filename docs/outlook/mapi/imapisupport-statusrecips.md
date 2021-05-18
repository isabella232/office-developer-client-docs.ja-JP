---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408769"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="f9fb5-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="f9fb5-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="f9fb5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9fb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9fb5-105">配信レポートと配信以外のレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="f9fb5-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f9fb5-106">Parameters</span></span>

 <span data-ttu-id="f9fb5-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="f9fb5-107">_lpMessage_</span></span>
  
> <span data-ttu-id="f9fb5-108">[in]レポートを生成するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="f9fb5-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="f9fb5-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="f9fb5-110">[in]_lpMessage_ が指すメッセージの受信者を表す [ADRLIST](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9fb5-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="f9fb5-111">Return value</span></span>

<span data-ttu-id="f9fb5-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9fb5-112">S_OK</span></span> 
  
> <span data-ttu-id="f9fb5-113">レポートが正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="f9fb5-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="f9fb5-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="f9fb5-115">呼び出しは全体的に成功しましたが、この種類の受信者の受信者オプションはありません。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="f9fb5-116">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f9fb5-117">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f9fb5-118">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9fb5-119">注釈</span><span class="sxs-lookup"><span data-stu-id="f9fb5-119">Remarks</span></span>

<span data-ttu-id="f9fb5-120">**IMAPISupport::StatusRecips** メソッドは、トランスポート プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="f9fb5-121">トランスポート プロバイダーは **StatusRecips** を呼び出して、MAPI がメッセージの 1 つ以上の受信者のセットに配信レポートまたは配信不能レポートを送信する要求を行います。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f9fb5-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f9fb5-122">Notes to callers</span></span>

<span data-ttu-id="f9fb5-123">メッセージの処理 **中に StatusRecips** を複数回呼び出す場合があります。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="f9fb5-124">ただし、開いているメッセージの **StatusRecips** を呼び出す場合は、メッセージ受信者のすべての配信情報と配信不能情報を収集し、その受信者リストの **StatusRecips** を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="f9fb5-125">1 つの受信者に対して複数の **StatusRecips** 呼び出しを実行すると、複数の同一のレポートが送信される可能性があるため、コレクションの 1 つのポイントが重要です。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="f9fb5-126">_lpRecipList_ パラメーターで示される **ADRLIST** 構造体のメッセージ配信または配信不能に関連するプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="f9fb5-127">配信レポートと配信以外のレポートに必要なプロパティとオプションのプロパティの完全な一覧[](required-report-message-properties.md)については、「必須レポート メッセージのプロパティ」および「オプションのレポート メッセージのプロパティ」[を参照してください](optional-report-message-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="f9fb5-128">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数と [MAPIAllocateMore](mapiallocatemore.md)関数を使用して _、lpRecipList_ の **ADRLIST** 構造体のメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="f9fb5-129">MAPI は **、StatusRecips** が成功した場合にのみ [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによってメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="f9fb5-130">配信レポートと配信以外のレポートの概要については、「MAPI レポート [メッセージ」を参照してください](mapi-report-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="f9fb5-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9fb5-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="f9fb5-131">See also</span></span>



[<span data-ttu-id="f9fb5-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="f9fb5-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="f9fb5-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="f9fb5-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="f9fb5-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="f9fb5-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="f9fb5-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="f9fb5-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="f9fb5-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="f9fb5-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="f9fb5-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="f9fb5-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="f9fb5-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f9fb5-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f9fb5-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9fb5-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

