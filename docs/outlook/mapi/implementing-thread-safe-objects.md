---
title: スレッドセーフオブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c911694-b953-4d35-9a3a-22c17cfd79bc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9160136542c7960bad0be2423872171b17d99fe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310039"
---
# <a name="implementing-thread-safe-objects"></a><span data-ttu-id="1761e-103">スレッドセーフオブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="1761e-103">Implementing Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="1761e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1761e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1761e-105">インターフェイスメソッドの呼び出しから直接取得されるオブジェクトの場合は、スレッドセーフを確実にするためにプロバイダーが責任を負っています。</span><span class="sxs-lookup"><span data-stu-id="1761e-105">With objects that are returned from interface method calls directly, it is the provider's responsibility to ensure thread-safety.</span></span> <span data-ttu-id="1761e-106">コールバックオブジェクトを使用すると、クライアントアプリケーションの責任を負うことになります。</span><span class="sxs-lookup"><span data-stu-id="1761e-106">With callback objects, it is the client application's responsibility.</span></span>
  
<span data-ttu-id="1761e-107">クライアントは、MAPI ユーティリティ[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出すことによって、スレッドセーフな通知コールバックを実装できます。</span><span class="sxs-lookup"><span data-stu-id="1761e-107">A client can implement a thread-safe notification callback by calling the MAPI utility [HrThisThreadAdviseSink](hrthisthreadadvisesink.md).</span></span> <span data-ttu-id="1761e-108">**HrThisThreadAdviseSink**は、スレッドセーフでないアドバイズシンクをスレッドセーフなアドバイズシンクに変換します。</span><span class="sxs-lookup"><span data-stu-id="1761e-108">**HrThisThreadAdviseSink** transforms a non-thread-safe advise sink into a thread-safe one.</span></span> <span data-ttu-id="1761e-109">進行状況のコールバックの場合は、このようなユーティリティはありません。</span><span class="sxs-lookup"><span data-stu-id="1761e-109">For progress callbacks, there is no such utility.</span></span> <span data-ttu-id="1761e-110">クライアントは、MAPI スレッドセーフの進行状況オブジェクトを使用するか、手動で作成するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1761e-110">A client can choose to use the MAPI thread-safe progress object or create one manually.</span></span> 
  
<span data-ttu-id="1761e-111">スレッドセーフオブジェクトは、スレッドに対応している場合もあります。</span><span class="sxs-lookup"><span data-stu-id="1761e-111">A thread-safe object might or might not also be thread-aware.</span></span> <span data-ttu-id="1761e-112">スレッド対応オブジェクトは、それを使用しているすべてのスレッドに対して個別のコンテキストを保持します。</span><span class="sxs-lookup"><span data-stu-id="1761e-112">A thread-aware object maintains a separate context for every thread that is using it.</span></span> <span data-ttu-id="1761e-113">スレッドセーフなオブジェクトでスレッドを認識する必要はありませんが、スレッドの認識をサポートすることは状況によっては役に立ちません。</span><span class="sxs-lookup"><span data-stu-id="1761e-113">Service providers are not required to support thread-awareness in their thread-safe objects, although supporting thread-awareness can be useful in some situations.</span></span> <span data-ttu-id="1761e-114">2つの MAPI テーブルでは、定義によって常に独自のコンテキストが提供されます。</span><span class="sxs-lookup"><span data-stu-id="1761e-114">Two MAPI tables always provide their own context by definition.</span></span> <span data-ttu-id="1761e-115">別のスレッドで使用される1つのテーブルは、一意のコンテキストを提供しません。</span><span class="sxs-lookup"><span data-stu-id="1761e-115">One table used on different threads does not and should not provide unique context.</span></span>
  
<span data-ttu-id="1761e-116">クライアントは、 **MAPIInitialize**呼び出しに使用したのと同じスレッドで通知を受信するか、**アドバイズ**呼び出しに使用されたものと同じスレッドで、または MAPI が所有する別のスレッドで通知を受信するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1761e-116">A client can choose between receiving notifications on the same thread that was used for the **MAPIInitialize** call, on the same thread that was used for the **Advise** call, or on a separate thread owned by MAPI.</span></span> <span data-ttu-id="1761e-117">**MAPIInitialize**の呼び出しに使用したのと同じスレッドに通知が配信されるようにするために、クライアントは[MAPIInitialize](mapiinitialize.md)を呼び出し、 [MAPIINIT_0](mapiinit_0.md)構造の**ulflags**メンバーに0を渡します。</span><span class="sxs-lookup"><span data-stu-id="1761e-117">To ensure that notifications arrive on the same thread that was used to call **MAPIInitialize**, a client calls [MAPIInitialize](mapiinitialize.md) and passes zero in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="1761e-118">通知は、メインメッセージループ中に配信されます。</span><span class="sxs-lookup"><span data-stu-id="1761e-118">Notifications are then delivered during the main message loop.</span></span> 
  
<span data-ttu-id="1761e-119">MAPI が所有するスレッドで通知を受信するために、クライアントは**MAPIINIT_0**構造体の**ulflags**メンバーを MAPI_MULTITHREAD_NOTIFICATIONS に設定して**MAPIInitialize**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1761e-119">To receive notifications on the MAPI-owned thread, a client calls **MAPIInitialize** with the **ulFlags** member of the **MAPIINIT_0** structure set to MAPI_MULTITHREAD_NOTIFICATIONS.</span></span> <span data-ttu-id="1761e-120">**アドバイズ**呼び出しは、ラップされたバージョンではなく、クライアントのアドバイズシンクオブジェクトで行われます。</span><span class="sxs-lookup"><span data-stu-id="1761e-120">The **Advise** call is made with the client's advise sink object rather than a wrapped version.</span></span> 
  
<span data-ttu-id="1761e-121">通知が**アドバイズ**に使用されたのと同じスレッドに到着するように、クライアントは[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出し、新しく作成されたラップアドバイズシンクを、元のアドバイズシンクではなく**アドバイズ**に渡します。</span><span class="sxs-lookup"><span data-stu-id="1761e-121">To ensure that notifications arrive on the same thread that was used to call **Advise**, a client calls [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) and passes the newly created wrapped advise sink to **Advise** rather than the original advise sink.</span></span> <span data-ttu-id="1761e-122">**MAPIInitialize**は、フラグの値を使用して呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="1761e-122">**MAPIInitialize** can be called with either flag value.</span></span> 
  

