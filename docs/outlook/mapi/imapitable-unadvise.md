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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430232"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="09614-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="09614-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="09614-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09614-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09614-105">[IMAPITable::Advise](imapitable-advise.md)メソッドへの呼び出しで以前に設定された通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="09614-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="09614-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="09614-106">Parameters</span></span>

 <span data-ttu-id="09614-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="09614-107">_ulConnection_</span></span>
  
> <span data-ttu-id="09614-108">[in] [IMAPITable::Advise](imapitable-advise.md)への呼び出しによって返される登録接続の数。</span><span class="sxs-lookup"><span data-stu-id="09614-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09614-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="09614-109">Return value</span></span>

<span data-ttu-id="09614-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="09614-110">S_OK</span></span> 
  
> <span data-ttu-id="09614-111">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="09614-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09614-112">注釈</span><span class="sxs-lookup"><span data-stu-id="09614-112">Remarks</span></span>

<span data-ttu-id="09614-113">**IMAPITable::Unadvise** メソッドを使用して **、IMAPITable::Advise** の前の呼び出しで _lpAdviseSink_ パラメーターで渡されたアアドバイス シンク オブジェクトへのポインターを解放し、通知登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="09614-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="09614-114">アアドバイス シンク オブジェクトへのポインターを破棄する一環として、オブジェクトの **IUnknown::Release** メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="09614-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="09614-115">一般に **、Unadvise** 呼び出し中に Release が呼び出されますが、別のスレッドがアドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合 **、OnNotify** メソッドが返されるまで、Release 呼び出しは遅延されます。 </span><span class="sxs-lookup"><span data-stu-id="09614-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="09614-116">通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。</span><span class="sxs-lookup"><span data-stu-id="09614-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="09614-117">テーブル通知の詳細については、「テーブル通知について [」を参照してください](about-table-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="09614-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="09614-118">**IMAPISupport メソッドを使用して通知を** サポートする方法については、「Support Event Notification 」[を参照してください](supporting-event-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="09614-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09614-119">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="09614-119">MFCMAPI reference</span></span>

<span data-ttu-id="09614-120">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09614-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09614-121">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="09614-121">**File**</span></span>|<span data-ttu-id="09614-122">**関数**</span><span class="sxs-lookup"><span data-stu-id="09614-122">**Function**</span></span>|<span data-ttu-id="09614-123">**コメント**</span><span class="sxs-lookup"><span data-stu-id="09614-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09614-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="09614-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="09614-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="09614-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="09614-126">MFCMAPI は **IMAPITable::Unadvise** メソッドを使用して、テーブルの通知をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="09614-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09614-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="09614-127">See also</span></span>



[<span data-ttu-id="09614-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="09614-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="09614-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="09614-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="09614-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09614-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="09614-131">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="09614-131">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

