---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ebde06d0d22320ecb5edb633cf8d04aaeec2a841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433984"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="239ae-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="239ae-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="239ae-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="239ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="239ae-105">現在のメッセージが MAPI スプーラーに送信されたとフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="239ae-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="239ae-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="239ae-106">Parameters</span></span>

<span data-ttu-id="239ae-107">なし</span><span class="sxs-lookup"><span data-stu-id="239ae-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="239ae-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="239ae-108">Return value</span></span>

<span data-ttu-id="239ae-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="239ae-109">S_OK</span></span> 
  
> <span data-ttu-id="239ae-110">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="239ae-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="239ae-111">注釈</span><span class="sxs-lookup"><span data-stu-id="239ae-111">Remarks</span></span>

<span data-ttu-id="239ae-112">フォーム オブジェクトは [、IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)の呼び出しが正常に返された後 **、IMAPIViewAdviseSink::OnSubmitted** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="239ae-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="239ae-113">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="239ae-113">Notes to implementers</span></span>

<span data-ttu-id="239ae-114">**OnSubmitted が** 呼び出された後、メッセージが更新されたという前提で続行できます。</span><span class="sxs-lookup"><span data-stu-id="239ae-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="239ae-115">発生した変更を反映するようにウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="239ae-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="239ae-116">フォーム通知の詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="239ae-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="239ae-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="239ae-117">See also</span></span>



[<span data-ttu-id="239ae-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="239ae-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="239ae-119">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="239ae-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

