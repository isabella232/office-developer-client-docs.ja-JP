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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329485"
---
# <a name="imapiformadvise"></a><span data-ttu-id="4d6b4-103">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="4d6b4-103">IMAPIForm::Advise</span></span>

  
  
<span data-ttu-id="4d6b4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d6b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d6b4-105">フォームに影響を与えるイベントに関する通知用にフォーム ビューアーを登録します。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-105">Registers a form viewer for notifications about events that affect the form.</span></span>
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="4d6b4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4d6b4-106">Parameters</span></span>

 <span data-ttu-id="4d6b4-107">_pAdvise_</span><span class="sxs-lookup"><span data-stu-id="4d6b4-107">_pAdvise_</span></span>
  
> <span data-ttu-id="4d6b4-108">[in]ビューへのポインターは、後続の通知を受け取るシンク オブジェクトに通知します。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-108">[in] A pointer to a view advise sink object to receive the subsequent notifications.</span></span> 
    
 <span data-ttu-id="4d6b4-109">_pulConnection_</span><span class="sxs-lookup"><span data-stu-id="4d6b4-109">_pulConnection_</span></span>
  
> <span data-ttu-id="4d6b4-110">[out]正常な通知登録を表す 0 以外の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-110">[out] A pointer to a nonzero value that represents a successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d6b4-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="4d6b4-111">Return value</span></span>

<span data-ttu-id="4d6b4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d6b4-112">S_OK</span></span> 
  
> <span data-ttu-id="4d6b4-113">登録が成功しました。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-113">The registration was successful.</span></span>
    
<span data-ttu-id="4d6b4-114">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="4d6b4-114">E_OUTOFMEMORY</span></span> 
  
> <span data-ttu-id="4d6b4-115">メモリ不足のため、登録が失敗しました。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-115">The registration was unsuccessful because of insufficient memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d6b4-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4d6b4-116">Remarks</span></span>

<span data-ttu-id="4d6b4-117">フォームビューアーは、フォームの **IMAPIForm::Advise** メソッドを呼び出して、フォームに変更が発生した場合に通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-117">Form viewers call a form's **IMAPIForm::Advise** method to register for notification when changes occur to the form.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4d6b4-118">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="4d6b4-118">Notes to implementers</span></span>

<span data-ttu-id="4d6b4-119">イベントが発生した場合に適切な [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md)メソッドを呼び出す際に使用できるよう _、pAdvise_ パラメーターで渡されたビューアアドバイス シンク ポインターのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-119">Keep a copy of the view advise sink pointer passed in the  _pAdvise_ parameter so that you can use it to call the appropriate [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) method when an event occurs.</span></span> <span data-ttu-id="4d6b4-120">通知の登録が取り消されるまでポインターを保持するには、ビュー アアドバイス シンクの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-120">Call the view advise sink's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to retain the pointer until notification registration is canceled.</span></span> <span data-ttu-id="4d6b4-121">_pulConnection パラメーターの内容を_ 0 以外の数値に設定します。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-121">Set the contents of the  _pulConnection_ parameter to a nonzero number.</span></span> 
  
<span data-ttu-id="4d6b4-122">多くのフォームでは、イベントの登録および後続の通知を処理するヘルパー オブジェクトを実装しています。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-122">Many forms implement a helper object to handle the registration and subsequent notification of events.</span></span> 
  
<span data-ttu-id="4d6b4-123">通知プロセス全般の詳細については [、「MAPI でのイベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-123">For more information about the notification process in general, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> 
  
<span data-ttu-id="4d6b4-124">通知とフォームの詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="4d6b4-124">For more information about notification and forms, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4d6b4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d6b4-125">See also</span></span>



[<span data-ttu-id="4d6b4-126">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4d6b4-126">IMAPIForm::Unadvise</span></span>](imapiform-unadvise.md)
  
[<span data-ttu-id="4d6b4-127">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d6b4-127">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="4d6b4-128">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d6b4-128">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="4d6b4-129">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="4d6b4-129">Event Notification in MAPI</span></span>](event-notification-in-mapi.md)
  
[<span data-ttu-id="4d6b4-130">フォーム通知の送受信</span><span class="sxs-lookup"><span data-stu-id="4d6b4-130">Sending and Receiving Form Notifications</span></span>](sending-and-receiving-form-notifications.md)

