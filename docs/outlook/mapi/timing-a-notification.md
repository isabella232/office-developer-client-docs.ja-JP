---
title: 通知のタイミング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6981a3b0-96eb-44a2-b051-1c5efc70e9e3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fa3b155820c64ff55e324c5611eed7348cb93e2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411149"
---
# <a name="timing-a-notification"></a><span data-ttu-id="d05cb-103">通知のタイミング</span><span class="sxs-lookup"><span data-stu-id="d05cb-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="d05cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d05cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d05cb-105">イベント通知は非同期プロセスなので、イベントが発生した直後ではなく、いつでも通知できます。</span><span class="sxs-lookup"><span data-stu-id="d05cb-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="d05cb-106">[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドへの呼び出しのタイミングは、アドバイス ソースを実装するサービス プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="d05cb-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="d05cb-107">サービス プロバイダーは、次のいずれかの方法でクライアントに通知できます。</span><span class="sxs-lookup"><span data-stu-id="d05cb-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="d05cb-108">イベントと同時に。</span><span class="sxs-lookup"><span data-stu-id="d05cb-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="d05cb-109">イベントの直後。</span><span class="sxs-lookup"><span data-stu-id="d05cb-109">Directly after the event.</span></span>
    
- <span data-ttu-id="d05cb-110">イベントに続く後の時点で、おそらく **Unadvise 呼び出しの後** 。</span><span class="sxs-lookup"><span data-stu-id="d05cb-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="d05cb-111">ほとんどのサービス プロバイダーは、イベントを担当する MAPI メソッドが呼び出し元に戻った後に **OnNotify** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d05cb-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="d05cb-112">たとえば、メッセージへの変更が保存された場合 [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) 呼び出し後、または **IUnknown::Release** 呼び出し後にメッセージが解放された場合に、メッセージに対する通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="d05cb-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="d05cb-113">通知が送信されるまで、メッセージ ストアに変更は表示されません。</span><span class="sxs-lookup"><span data-stu-id="d05cb-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="d05cb-114">登録を取り消す **Unadvise** を呼び出した後、アドバイス ソースから通知を受信できます。</span><span class="sxs-lookup"><span data-stu-id="d05cb-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="d05cb-115">**Unadvise** の正常な呼び出しに従うのではなく、参照カウントが 0 に落ちた後にのみ、アドバイス シンクを解放してください。</span><span class="sxs-lookup"><span data-stu-id="d05cb-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="d05cb-116">**Unadvise** を呼び出したので、アアドバイス シンクは不要になったと仮定して下さい。</span><span class="sxs-lookup"><span data-stu-id="d05cb-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

