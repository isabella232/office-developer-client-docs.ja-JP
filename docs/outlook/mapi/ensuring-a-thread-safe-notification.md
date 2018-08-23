---
title: スレッド セーフ通知の確認
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 70e594057f2d654e0527b0caa0951e44842df809
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800004"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="76a77-103">スレッド セーフ通知の確認</span><span class="sxs-lookup"><span data-stu-id="76a77-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="76a77-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76a77-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76a77-105">クライアントは、マルチ スレッドのプラットフォームで実行している場合は、特定のスレッドで、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドの呼び出しが発生することを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76a77-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="76a77-106">**OnNotify**への呼び出しは、任意のスレッドで発生することが通常、ために、エラーの原因をデバッグするが難しいことと、予期しない、望ましくないスレッドで通知を受信することができます。</span><span class="sxs-lookup"><span data-stu-id="76a77-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="76a77-107">**アドバイズ**するために使用されたのと同じスレッドで呼び出し、**アドバイズ**を呼び出す前に[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出して、 **OnNotify**に特定の通知のための呼び出しが行われていることを保証します。</span><span class="sxs-lookup"><span data-stu-id="76a77-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="76a77-108">* * * * HrThisThreadAdviseSink。 アドバイズ シンク オブジェクトから新しいアドバイズ シンク オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="76a77-108">** **HrThisThreadAdviseSink**** creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="76a77-109">**Advise**への呼び出しでは、この新しいオブジェクトを渡します。</span><span class="sxs-lookup"><span data-stu-id="76a77-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="76a77-110">アドバイズ シンクが動作しない可能性の特定のスレッドのコンテキストの外部のオブジェクトは常に登録する必要がありますが、すべてのクライアントは、 **HrThisThreadAdviseSink**で作成したシンク オブジェクトを案内します。</span><span class="sxs-lookup"><span data-stu-id="76a77-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

