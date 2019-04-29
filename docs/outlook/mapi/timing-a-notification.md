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
# <a name="timing-a-notification"></a><span data-ttu-id="632cc-103">通知のタイミング</span><span class="sxs-lookup"><span data-stu-id="632cc-103">Timing a Notification</span></span>

  
  
<span data-ttu-id="632cc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="632cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="632cc-105">イベント通知は非同期プロセスなので、いつでもイベントが発生した直後に通知することはできません。</span><span class="sxs-lookup"><span data-stu-id="632cc-105">Because event notification is an asynchronous process, you can be notified at any time, not necessarily immediately after the event has occurred.</span></span>
  
 <span data-ttu-id="632cc-106">[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドの呼び出しのタイミングは、アドバイズソースを実装するサービスプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="632cc-106">The timing of calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method varies depending on the service provider implementing the advise source.</span></span> <span data-ttu-id="632cc-107">サービスプロバイダーは、クライアントに次のいずれかを通知できます。</span><span class="sxs-lookup"><span data-stu-id="632cc-107">Service providers can notify your client either:</span></span> 
  
- <span data-ttu-id="632cc-108">イベントと同時に実行します。</span><span class="sxs-lookup"><span data-stu-id="632cc-108">Simultaneously with the event.</span></span>
    
- <span data-ttu-id="632cc-109">イベントの直後。</span><span class="sxs-lookup"><span data-stu-id="632cc-109">Directly after the event.</span></span>
    
- <span data-ttu-id="632cc-110">後で、**アドバイズ**中止呼び出しの後に、イベントをフォローすることがあります。</span><span class="sxs-lookup"><span data-stu-id="632cc-110">At some later point following the event, possibly after an **Unadvise** call.</span></span> 
    
<span data-ttu-id="632cc-111">ほとんどのサービスプロバイダーは、イベントを担当する MAPI メソッドが発信者に返された後に、 **onnotify**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="632cc-111">Most service providers call **OnNotify** after the MAPI method responsible for the event has returned to its caller.</span></span> <span data-ttu-id="632cc-112">たとえば、メッセージに対する変更が保存されたとき、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しの後、またはメッセージが解放されたときに、 **IUnknown:: Release**呼び出しの後にメッセージの通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="632cc-112">For example, notifications on messages are sent either when changes to the message are saved, after the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call, or when the message is released, after the **IUnknown::Release** call.</span></span> <span data-ttu-id="632cc-113">通知が送信されるまで、メッセージストアに変更は表示されません。</span><span class="sxs-lookup"><span data-stu-id="632cc-113">Until the notification is sent, no changes are visible in the message store.</span></span> 
  
<span data-ttu-id="632cc-114">**アドバイズ**中止を呼び出して登録をキャンセルした後、アドバイズソースから通知を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="632cc-114">You can receive notifications from an advise source after you have called **Unadvise** to cancel a registration.</span></span> <span data-ttu-id="632cc-115">アドバイズシンクは、その参照カウントが0に落ちた後にのみリリースし、**アドバイズ**中止の呼び出しが成功していないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="632cc-115">Be sure to release your advise sink only after its reference count has fallen to zero, not following a successful **Unadvise** call.</span></span> <span data-ttu-id="632cc-116">アドバイズシンクが不要になったため、**アドバイズ**中止を呼び出していることを前提としていません。</span><span class="sxs-lookup"><span data-stu-id="632cc-116">Do not assume that because you have called **Unadvise** that the advise sink is no longer necessary.</span></span> 
  

