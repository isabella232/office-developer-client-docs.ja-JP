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
ms.openlocfilehash: 7de4d3c58d5eeefcf9a82235333da5db4703bc8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592977"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="fecc1-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="fecc1-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="fecc1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fecc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fecc1-105">[IMAPITable::Advise](imapitable-advise.md)メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="fecc1-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="fecc1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fecc1-106">Parameters</span></span>

 <span data-ttu-id="fecc1-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="fecc1-107">_ulConnection_</span></span>
  
> <span data-ttu-id="fecc1-108">[in][IMAPITable::Advise](imapitable-advise.md)への呼び出しによって返された登録接続の数です。</span><span class="sxs-lookup"><span data-stu-id="fecc1-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fecc1-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fecc1-109">Return value</span></span>

<span data-ttu-id="fecc1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fecc1-110">S_OK</span></span> 
  
> <span data-ttu-id="fecc1-111">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="fecc1-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fecc1-112">注釈</span><span class="sxs-lookup"><span data-stu-id="fecc1-112">Remarks</span></span>

<span data-ttu-id="fecc1-113">**IMAPITable::Advise**通知の登録をキャンセルするために以前の呼び出しで_lpAdviseSink_パラメーターで渡されたアドバイズ シンク オブジェクトへのポインターを解放するのにには、 **IMAPITable::Unadvise**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fecc1-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="fecc1-114">アドバイズ シンク オブジェクトへのポインターを破棄することの一環として、オブジェクト**が**呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fecc1-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="fecc1-115">**リリース**が呼び出される一般的には、別のスレッドがいる、アドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す場合は、 **Unadvise**の呼び出し中に**リリース**の呼び出し、 **OnNotify**まで延期メソッドを返します。</span><span class="sxs-lookup"><span data-stu-id="fecc1-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="fecc1-116">通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fecc1-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="fecc1-117">テーブル通知の詳細については、[テーブルについての通知](about-table-notifications.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fecc1-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="fecc1-118">通知をサポートするために**IMAPISupport**メソッドを使用する方法の詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fecc1-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fecc1-119">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="fecc1-119">MFCMAPI reference</span></span>

<span data-ttu-id="fecc1-120">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="fecc1-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fecc1-121">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="fecc1-121">**File**</span></span>|<span data-ttu-id="fecc1-122">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="fecc1-122">**Function**</span></span>|<span data-ttu-id="fecc1-123">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="fecc1-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fecc1-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="fecc1-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="fecc1-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="fecc1-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="fecc1-126">MFCMAPI では、 **IMAPITable::Unadvise**メソッドを使用して、テーブルの通知をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="fecc1-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fecc1-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="fecc1-127">See also</span></span>



[<span data-ttu-id="fecc1-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="fecc1-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="fecc1-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="fecc1-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="fecc1-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fecc1-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="fecc1-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="fecc1-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

