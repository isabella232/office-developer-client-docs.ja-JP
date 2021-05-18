---
title: オブジェクトのThread-Safe実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413529"
---
# <a name="implementing-thread-safe-objects"></a><span data-ttu-id="2f159-103">オブジェクトのThread-Safe実装</span><span class="sxs-lookup"><span data-stu-id="2f159-103">Implementing Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="2f159-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f159-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f159-105">インターフェイス メソッドから返されるオブジェクトが直接呼び出される場合、スレッドセーフを確保する責任はプロバイダーの責任です。</span><span class="sxs-lookup"><span data-stu-id="2f159-105">With objects that are returned from interface method calls directly, it is the provider's responsibility to ensure thread-safety.</span></span> <span data-ttu-id="2f159-106">コールバック オブジェクトでは、クライアント アプリケーションの責任です。</span><span class="sxs-lookup"><span data-stu-id="2f159-106">With callback objects, it is the client application's responsibility.</span></span>
  
<span data-ttu-id="2f159-107">クライアントは、MAPI ユーティリティ [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出すことによって、スレッド セーフな通知コールバックを実装できます。</span><span class="sxs-lookup"><span data-stu-id="2f159-107">A client can implement a thread-safe notification callback by calling the MAPI utility [HrThisThreadAdviseSink](hrthisthreadadvisesink.md).</span></span> <span data-ttu-id="2f159-108">**HrThisThreadAdviseSink** は、スレッド セーフでないアドバイス シンクをスレッド セーフに変換します。</span><span class="sxs-lookup"><span data-stu-id="2f159-108">**HrThisThreadAdviseSink** transforms a non-thread-safe advise sink into a thread-safe one.</span></span> <span data-ttu-id="2f159-109">進行状況コールバックの場合、そのようなユーティリティはありません。</span><span class="sxs-lookup"><span data-stu-id="2f159-109">For progress callbacks, there is no such utility.</span></span> <span data-ttu-id="2f159-110">クライアントは、MAPI スレッド セーフの進行状況オブジェクトを使用するか、手動で作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="2f159-110">A client can choose to use the MAPI thread-safe progress object or create one manually.</span></span> 
  
<span data-ttu-id="2f159-111">スレッド セーフ オブジェクトは、スレッドを認識する場合と認識しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2f159-111">A thread-safe object might or might not also be thread-aware.</span></span> <span data-ttu-id="2f159-112">スレッド対応オブジェクトは、使用しているスレッドごとに個別のコンテキストを維持します。</span><span class="sxs-lookup"><span data-stu-id="2f159-112">A thread-aware object maintains a separate context for every thread that is using it.</span></span> <span data-ttu-id="2f159-113">サービス プロバイダーは、スレッド セーフ オブジェクトでスレッド認識をサポートする必要はありません。ただし、スレッド認識のサポートは状況によっては役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2f159-113">Service providers are not required to support thread-awareness in their thread-safe objects, although supporting thread-awareness can be useful in some situations.</span></span> <span data-ttu-id="2f159-114">2 つの MAPI テーブルは、定義によって常に独自のコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="2f159-114">Two MAPI tables always provide their own context by definition.</span></span> <span data-ttu-id="2f159-115">異なるスレッドで使用される 1 つのテーブルは、固有のコンテキストを提供する必要はありません。また、一意のコンテキストを提供する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2f159-115">One table used on different threads does not and should not provide unique context.</span></span>
  
<span data-ttu-id="2f159-116">クライアントは **、MAPIInitialize** 呼び出しに使用されたのと同じスレッド **、Advise** 呼び出しに使用されたスレッド、または MAPI が所有する別のスレッドで通知を受信する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="2f159-116">A client can choose between receiving notifications on the same thread that was used for the **MAPIInitialize** call, on the same thread that was used for the **Advise** call, or on a separate thread owned by MAPI.</span></span> <span data-ttu-id="2f159-117">**MAPIInitialize** の呼び出しに使用されたスレッドと同じスレッドに通知が確実に届くには、クライアントが [MAPIInitialize](mapiinitialize.md)を呼び出し、MAPIINIT_0 構造体の **ulFlags** メンバーで [0 を渡](mapiinit_0.md)します。</span><span class="sxs-lookup"><span data-stu-id="2f159-117">To ensure that notifications arrive on the same thread that was used to call **MAPIInitialize**, a client calls [MAPIInitialize](mapiinitialize.md) and passes zero in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="2f159-118">その後、メイン メッセージ ループ中に通知が配信されます。</span><span class="sxs-lookup"><span data-stu-id="2f159-118">Notifications are then delivered during the main message loop.</span></span> 
  
<span data-ttu-id="2f159-119">MAPI が所有するスレッドで通知を受信するには、クライアントが **MAPIInitialize** を呼び出し **、MAPIINIT_0** 構造体の **ulFlags** メンバーを MAPI_MULTITHREAD_NOTIFICATIONS に設定します。</span><span class="sxs-lookup"><span data-stu-id="2f159-119">To receive notifications on the MAPI-owned thread, a client calls **MAPIInitialize** with the **ulFlags** member of the **MAPIINIT_0** structure set to MAPI_MULTITHREAD_NOTIFICATIONS.</span></span> <span data-ttu-id="2f159-120">**Advise 呼び** 出しは、ラップされたバージョンではなく、クライアントのアアドバイス シンク オブジェクトで行います。</span><span class="sxs-lookup"><span data-stu-id="2f159-120">The **Advise** call is made with the client's advise sink object rather than a wrapped version.</span></span> 
  
<span data-ttu-id="2f159-121">**通知** が、Advise を呼び出すのに使用されたスレッドと同じスレッドに確実に到着するために、クライアントは [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出し、新しく作成されたラップされたアアドバイス シンクを元のアアドバイス シンクではなく、アドバイスに渡します。</span><span class="sxs-lookup"><span data-stu-id="2f159-121">To ensure that notifications arrive on the same thread that was used to call **Advise**, a client calls [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) and passes the newly created wrapped advise sink to **Advise** rather than the original advise sink.</span></span> <span data-ttu-id="2f159-122">**MAPIInitialize は** 、いずれかのフラグ値で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2f159-122">**MAPIInitialize** can be called with either flag value.</span></span> 
  

