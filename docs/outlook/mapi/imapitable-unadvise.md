---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328806"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="83807-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="83807-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="83807-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83807-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83807-105">[IMAPITable:: Advise](imapitable-advise.md)メソッドへの呼び出しを使用して、以前に設定した通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="83807-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="83807-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83807-106">Parameters</span></span>

 <span data-ttu-id="83807-107">_ulconnection_</span><span class="sxs-lookup"><span data-stu-id="83807-107">_ulConnection_</span></span>
  
> <span data-ttu-id="83807-108">順番[IMAPITable:: Advise](imapitable-advise.md)への呼び出しによって返される登録接続の番号。</span><span class="sxs-lookup"><span data-stu-id="83807-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="83807-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="83807-109">Return value</span></span>

<span data-ttu-id="83807-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="83807-110">S_OK</span></span> 
  
> <span data-ttu-id="83807-111">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="83807-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="83807-112">解説</span><span class="sxs-lookup"><span data-stu-id="83807-112">Remarks</span></span>

<span data-ttu-id="83807-113">**imapitable:: アドバイズ**中止メソッドを使用して、前述の**IMAPITable:: advise**の呼び出しで_lpAdviseSink_パラメーターで渡されたアドバイズシンクオブジェクトへのポインターを解放し、通知登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="83807-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="83807-114">アドバイズシンクオブジェクトへのポインターを破棄する一環として、オブジェクトの**IUnknown:: Release**メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="83807-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="83807-115">通常、**リリース**は、**アドバイズ**中止の呼び出し中に呼び出されますが、別のスレッドがアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合は、 **onnotify**になるまで**release**呼び出しが遅延します。メソッドはを返します。</span><span class="sxs-lookup"><span data-stu-id="83807-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="83807-116">通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83807-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="83807-117">テーブル通知に関する特定の情報については、「[テーブル通知につい](about-table-notifications.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83807-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="83807-118">**imapisupport**メソッドを使用して通知をサポートする方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83807-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="83807-119">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="83807-119">MFCMAPI reference</span></span>

<span data-ttu-id="83807-120">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83807-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="83807-121">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="83807-121">**File**</span></span>|<span data-ttu-id="83807-122">**関数**</span><span class="sxs-lookup"><span data-stu-id="83807-122">**Function**</span></span>|<span data-ttu-id="83807-123">**コメント**</span><span class="sxs-lookup"><span data-stu-id="83807-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="83807-124">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="83807-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="83807-125">CContentsTableListCtrl:: notificationoff</span><span class="sxs-lookup"><span data-stu-id="83807-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="83807-126">mfcmapi は、 **IMAPITable:: アドバイズ**中止メソッドを使用して、テーブルの通知を取り消します。</span><span class="sxs-lookup"><span data-stu-id="83807-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83807-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="83807-127">See also</span></span>



[<span data-ttu-id="83807-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="83807-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="83807-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="83807-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="83807-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="83807-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="83807-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="83807-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

