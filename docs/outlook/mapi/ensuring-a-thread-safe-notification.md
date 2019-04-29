---
title: スレッドセーフ通知の確認
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
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="87dab-103">スレッドセーフ通知の確認</span><span class="sxs-lookup"><span data-stu-id="87dab-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="87dab-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87dab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87dab-105">クライアントがマルチスレッドのプラットフォームで実行されている場合は、特定のスレッドで[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドが呼び出されることを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87dab-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="87dab-106">通常、 **onnotify**への呼び出しはすべてのスレッドで発生するため、予期しない不要なスレッドで通知を受信し、デバッグが困難なエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="87dab-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="87dab-107">通知呼び出しに使用したのと同じスレッドで、特定の通知に対する**onnotify**への呼び出し\*\*\*\* が行われることを保証するには、 **advise**を呼び出す前に[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="87dab-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="87dab-108">\* \* \* \* HrThisThreadAdviseSink \* \* \* \* アドバイズシンクオブジェクトから新しいアドバイズシンクオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="87dab-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="87dab-109">この新しいオブジェクトを**Advise**の呼び出しで渡します。</span><span class="sxs-lookup"><span data-stu-id="87dab-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="87dab-110">特定のスレッドのコンテキストの外部では動作しない可能性があるアドバイズシンクオブジェクトを持つすべてのクライアントは、 **HrThisThreadAdviseSink**で作成されたアドバイズシンクオブジェクトを常に登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87dab-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

