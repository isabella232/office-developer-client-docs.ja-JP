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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341770"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="5d593-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="5d593-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="5d593-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d593-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d593-105">配信レポートおよび配信不能レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="5d593-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="5d593-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5d593-106">Parameters</span></span>

 <span data-ttu-id="5d593-107">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="5d593-107">_lpMessage_</span></span>
  
> <span data-ttu-id="5d593-108">順番レポートを生成するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5d593-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="5d593-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="5d593-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="5d593-110">順番_lpmessage_によって示されるメッセージの受信者を記述する[adrlist](adrlist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5d593-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5d593-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="5d593-111">Return value</span></span>

<span data-ttu-id="5d593-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d593-112">S_OK</span></span> 
  
> <span data-ttu-id="5d593-113">レポートが正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="5d593-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="5d593-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="5d593-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="5d593-115">呼び出しは全体的に成功しましたが、この種類の受信者のオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="5d593-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="5d593-116">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="5d593-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="5d593-117">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d593-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="5d593-118">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d593-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d593-119">解説</span><span class="sxs-lookup"><span data-stu-id="5d593-119">Remarks</span></span>

<span data-ttu-id="5d593-120">**imapisupport:: StatusRecips**メソッドは、トランスポートプロバイダーのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="5d593-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="5d593-121">トランスポートプロバイダーは、 **StatusRecips**を呼び出して、MAPI がメッセージの1つ以上の受信者に対して配信レポートまたは配信不能レポートを送信するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="5d593-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5d593-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5d593-122">Notes to callers</span></span>

<span data-ttu-id="5d593-123">**StatusRecips**は、メッセージの処理中に複数回呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5d593-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="5d593-124">ただし、開いているメッセージに対して**StatusRecips**を呼び出す場合は、メッセージの受信者のすべての配信および配信情報を収集し、その受信者リストの**StatusRecips**を呼び出すことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5d593-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="5d593-125">1つの受信者に対して複数の**StatusRecips**呼び出しを行うと、複数の同一のレポートが送信される可能性があるため、単一のコレクションのポイントが重要です。</span><span class="sxs-lookup"><span data-stu-id="5d593-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="5d593-126">_lpRecipList_パラメーターによって示される**adrlist**構造で、メッセージ配信または配信不能に関連するプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="5d593-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="5d593-127">配信レポートと配信不能レポートの必須およびオプションのプロパティの完全な一覧については、「[必須のレポートメッセージのプロパティ](required-report-message-properties.md)」および「[オプションのレポートメッセージのプロパティ](optional-report-message-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d593-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="5d593-128">[MAPIAllocateBuffer](mapiallocatebuffer.md)関数と[MAPIAllocateMore](mapiallocatemore.md)関数を使用して、 _lpRecipList_の**adrlist**構造のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5d593-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="5d593-129">MAPI では、 **StatusRecips**が正常に終了した場合にのみ[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによってメモリが解放されます。</span><span class="sxs-lookup"><span data-stu-id="5d593-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="5d593-130">配信レポートと配信不能レポートの概要については、「 [MAPI レポートメッセージ](mapi-report-messages.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d593-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5d593-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d593-131">See also</span></span>



[<span data-ttu-id="5d593-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="5d593-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="5d593-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="5d593-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="5d593-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="5d593-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="5d593-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="5d593-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="5d593-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5d593-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5d593-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="5d593-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="5d593-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5d593-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5d593-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d593-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

