---
title: 通知のThread-Safeする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424848"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="f3918-103">通知のThread-Safeする</span><span class="sxs-lookup"><span data-stu-id="f3918-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="f3918-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3918-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3918-105">クライアントがマルチスレッド プラットフォームで実行されている場合は [、IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドの呼び出しが特定のスレッドで発生することを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3918-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="f3918-106">**OnNotify** の呼び出しは通常、任意のスレッドで発生する可能性があります。予期しないスレッドや不要なスレッドに関する通知を受け取り、デバッグが困難なエラーにつながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f3918-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="f3918-107">特定の通知に対する **OnNotify** の呼び出しが **、Advise** 呼び出しに使用されたのと同じスレッドで行われることを保証するには、Advise を呼び出す前に [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) を呼び出 **します**。</span><span class="sxs-lookup"><span data-stu-id="f3918-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="f3918-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* は、アドバイス シンク オブジェクトから新しいアアドバイス シンク オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f3918-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="f3918-109">この新しいオブジェクトを呼び出しで Advise に **渡します**。</span><span class="sxs-lookup"><span data-stu-id="f3918-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="f3918-110">特定のスレッドのコンテキスト外で動作しない可能性があるシンク オブジェクトをアドバイスするクライアントはすべて **、HrThisThreadAdviseSink** で作成されたアアドバイス シンク オブジェクトを常に登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3918-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

