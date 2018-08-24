---
title: 通知のタイミング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b4b0292ab16eabe30755fe84885a29fb8e3ce295
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595196"
---
# <a name="timing-a-notification"></a><span data-ttu-id="b1d64-103">通知のタイミング</span><span class="sxs-lookup"><span data-stu-id="b1d64-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="b1d64-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1d64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1d64-105">イベント通知は非同期処理であるため、通知が可能、いつでも必ずしもイベントが発生した後にすぐにします。</span><span class="sxs-lookup"><span data-stu-id="b1d64-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="b1d64-106">[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドの呼び出しのタイミングは、アドバイスのソースを実装するサービス プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="b1d64-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="b1d64-107">サービス プロバイダーか、クライアントに通知できます。</span><span class="sxs-lookup"><span data-stu-id="b1d64-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="b1d64-108">イベントと同時に。</span><span class="sxs-lookup"><span data-stu-id="b1d64-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="b1d64-109">直後のイベントです。</span><span class="sxs-lookup"><span data-stu-id="b1d64-109">Directly after the event.</span></span>
    
- <span data-ttu-id="b1d64-110">ある後で時点で次のイベント可能性があります、 **Unadvise**の呼び出しの後です。</span><span class="sxs-lookup"><span data-stu-id="b1d64-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="b1d64-111">ほとんどのサービス プロバイダーは、イベントを行う MAPI メソッドは、呼び出し元に返された後、 **OnNotify**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b1d64-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="b1d64-112">などの**リ ス**を呼び出した後に、メッセージがリリースされたとき、またはメッセージへの変更を保存すると[IMAPIProp::SaveChanges](imapiprop-savechanges.md)の呼び出しの後、メッセージの通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="b1d64-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="b1d64-113">通知が送信されるまで変更は表示されません、メッセージ ・ ストアにします。</span><span class="sxs-lookup"><span data-stu-id="b1d64-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="b1d64-114">登録をキャンセルするのには**Unadvise**を呼び出した後、アドバイズ ソースから通知を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="b1d64-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="b1d64-115">その参照カウントがゼロ、従わない**Unadvise**の正常な呼び出しにやられた後にのみ、アドバイズ シンクを解放することを確認します。</span><span class="sxs-lookup"><span data-stu-id="b1d64-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="b1d64-116">**Unadvise**を呼び出す必要があるため、アドバイズ シンクを必要がなくなったとは限りません。</span><span class="sxs-lookup"><span data-stu-id="b1d64-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

