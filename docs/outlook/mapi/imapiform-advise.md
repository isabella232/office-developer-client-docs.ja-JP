---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800498"
---
# <a name="imapiformadvise"></a><span data-ttu-id="852d4-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="852d4-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="852d4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="852d4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="852d4-105">フォーム ビューアーの形式に影響するイベント通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="852d4-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="852d4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="852d4-106">Parameters</span></span>

 <span data-ttu-id="852d4-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="852d4-107">_pAdvise_</span></span>
  
> <span data-ttu-id="852d4-108">[in]ビューへのポインターでは、後続の通知を受信するシンク オブジェクトを案内します。</span><span class="sxs-lookup"><span data-stu-id="852d4-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="852d4-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="852d4-109">_pulConnection_</span></span>
  
> <span data-ttu-id="852d4-110">[out]成功した通知の登録を表す、0 以外の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="852d4-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="852d4-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="852d4-111">Return value</span></span>

<span data-ttu-id="852d4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="852d4-112">S_OK</span></span> 
  
> <span data-ttu-id="852d4-113">登録が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="852d4-113">The registration was successful.</span></span>
    
<span data-ttu-id="852d4-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="852d4-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="852d4-115">登録にメモリ不足のため失敗しました。</span><span class="sxs-lookup"><span data-stu-id="852d4-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="852d4-116">備考</span><span class="sxs-lookup"><span data-stu-id="852d4-116">Remarks</span></span>

<span data-ttu-id="852d4-117">フォーム ビューアーでは、フォームに変更が発生したときに通知を登録するのには、フォームの**IMAPIForm::Advise**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="852d4-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="852d4-118">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="852d4-118">Notes to implementers</span></span>

<span data-ttu-id="852d4-119">ビューのコピーを保存では、適切な[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md)メソッドを呼び出すイベントが発生したときにそれを使用できるように、 _pAdvise_パラメーターで渡されたシンク ポインターを案内します。</span><span class="sxs-lookup"><span data-stu-id="852d4-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="852d4-120">呼び出しビューは、通知の登録をキャンセルするまで、ポインターを保持するシンクの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx)の方法を案内します。</span><span class="sxs-lookup"><span data-stu-id="852d4-120">Call the view advise sink's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="852d4-121">_PulConnection_パラメーターの内容を 0 以外の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="852d4-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="852d4-122">多くのフォームは、登録とイベントの後続の通知を処理するヘルパー オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="852d4-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="852d4-123">通知プロセスの詳細については一般に、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="852d4-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="852d4-124">通知およびフォームの詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="852d4-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="852d4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="852d4-125">See also</span></span>



[<span data-ttu-id="852d4-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="852d4-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="852d4-127">IMAPIViewAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="852d4-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="852d4-128">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="852d4-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="852d4-129">MAPI でのイベントの通知</span><span class="sxs-lookup"><span data-stu-id="852d4-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="852d4-130">フォームの通知を送受信します。</span><span class="sxs-lookup"><span data-stu-id="852d4-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

