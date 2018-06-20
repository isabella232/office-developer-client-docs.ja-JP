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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 40a72bed0b3e763ea482b228174b85d9f42185c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800859"
---
# <a name="imapiviewadvisesinkonsubmitted"></a><span data-ttu-id="21f84-103">IMAPIViewAdviseSink::OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="21f84-103">IMAPIViewAdviseSink::OnSubmitted</span></span>

  
  
<span data-ttu-id="21f84-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21f84-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21f84-105">フォーム ビューアーの現在のメッセージが MAPI スプーラーに送信されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="21f84-105">Notifies the form viewer that the current message has been submitted to the MAPI spooler.</span></span>
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a><span data-ttu-id="21f84-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="21f84-106">Parameters</span></span>

<span data-ttu-id="21f84-107">なし</span><span class="sxs-lookup"><span data-stu-id="21f84-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="21f84-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="21f84-108">Return value</span></span>

<span data-ttu-id="21f84-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="21f84-109">S_OK</span></span> 
  
> <span data-ttu-id="21f84-110">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="21f84-110">The notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21f84-111">備考</span><span class="sxs-lookup"><span data-stu-id="21f84-111">Remarks</span></span>

<span data-ttu-id="21f84-112">フォーム オブジェクトは、 [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)への呼び出しが正常に返された後に、 **IMAPIViewAdviseSink::OnSubmitted**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="21f84-112">A form object calls the **IMAPIViewAdviseSink::OnSubmitted** method after a call to [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) has returned successfully.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="21f84-113">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="21f84-113">Notes to implementers</span></span>

<span data-ttu-id="21f84-114">**OnSubmitted**が呼び出されると、メッセージが更新されたことを前提として続行できます。</span><span class="sxs-lookup"><span data-stu-id="21f84-114">After **OnSubmitted** is called, you can continue on the assumption that the message has been updated.</span></span> <span data-ttu-id="21f84-115">発生した変更を反映するように、windows を更新します。</span><span class="sxs-lookup"><span data-stu-id="21f84-115">Update your windows to reflect any changes that have occurred.</span></span> 
  
<span data-ttu-id="21f84-116">フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21f84-116">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21f84-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="21f84-117">See also</span></span>



[<span data-ttu-id="21f84-118">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="21f84-118">IMAPIMessageSite::SubmitMessage</span></span>](imapimessagesite-submitmessage.md)
  
[<span data-ttu-id="21f84-119">IMAPIViewAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="21f84-119">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

