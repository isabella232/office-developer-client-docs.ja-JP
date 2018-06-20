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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f3642c890c3922611d57dea6f03aca5606876864
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800815"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="21090-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="21090-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="21090-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21090-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21090-105">配信し、配信不能レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="21090-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="21090-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="21090-106">Parameters</span></span>

 <span data-ttu-id="21090-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="21090-107">_lpMessage_</span></span>
  
> <span data-ttu-id="21090-108">[in]レポートを生成する対象のメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="21090-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="21090-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="21090-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="21090-110">[in]_LpMessage_が指すメッセージの受信者を記述する[ADRLIST](adrlist.md)構造体へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="21090-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="21090-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="21090-111">Return value</span></span>

<span data-ttu-id="21090-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="21090-112">S_OK</span></span> 
  
> <span data-ttu-id="21090-113">レポートが正常に生成されました。</span><span class="sxs-lookup"><span data-stu-id="21090-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="21090-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="21090-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="21090-115">呼び出しは完了しましたが、この種類の受信者の受信者のオプションはありません。</span><span class="sxs-lookup"><span data-stu-id="21090-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="21090-116">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21090-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="21090-117">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="21090-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="21090-118">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21090-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21090-119">備考</span><span class="sxs-lookup"><span data-stu-id="21090-119">Remarks</span></span>

<span data-ttu-id="21090-120">トランスポート プロバイダーのサポート オブジェクトの**IMAPISupport::StatusRecips**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="21090-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="21090-121">トランスポート プロバイダーは、その MAPI の送信を要求する**StatusRecips**の 1 つまたは複数のメッセージの受信者に配信または配信不能レポートを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="21090-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="21090-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="21090-122">Notes to callers</span></span>

<span data-ttu-id="21090-123">メッセージの処理中には、 **StatusRecips**を複数回呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="21090-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="21090-124">ただし、開いているメッセージの**StatusRecips**を呼び出すと場合、は、メッセージの受信者のすべての配信と配信不能の情報を収集し、その受信者のリストに**StatusRecips**を呼び出して、最善を行います。</span><span class="sxs-lookup"><span data-stu-id="21090-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="21090-125">コレクションの 1 つのポイントは重要ですが、1 人の受信者に複数の**StatusRecips**呼び出しで複数の同じレポートが送信されます。</span><span class="sxs-lookup"><span data-stu-id="21090-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="21090-126">メッセージの配信または_lpRecipList_パラメーターで指定された**ADRLIST**構造体で配信不能に関連するプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="21090-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="21090-127">配信レポートと配信不能レポートの必須およびオプションのプロパティの一覧は、[必要なレポートのメッセージのプロパティ](required-report-message-properties.md)と[オプションのレポート メッセージのプロパティ](optional-report-message-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21090-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="21090-128">[MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIAllocateMore](mapiallocatemore.md)関数を使用して、 _lpRecipList_の**ADRLIST**構造体のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="21090-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="21090-129">MAPI は、関数を呼び出して、 [MAPIFreeBuffer](mapifreebuffer.md) **StatusRecips**が成功した場合にのみメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="21090-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="21090-130">配信し、配信不能レポートの概要については、 [MAPI レポート メッセージ](mapi-report-messages.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21090-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21090-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="21090-131">See also</span></span>



[<span data-ttu-id="21090-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="21090-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="21090-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="21090-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="21090-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="21090-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="21090-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="21090-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="21090-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="21090-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="21090-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="21090-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="21090-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="21090-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="21090-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="21090-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

