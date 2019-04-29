---
title: 通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429160"
---
# <a name="handling-notifications"></a><span data-ttu-id="2ed08-103">通知の処理</span><span class="sxs-lookup"><span data-stu-id="2ed08-103">Handling notifications</span></span>

<span data-ttu-id="2ed08-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ed08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ed08-105">通知は、あるオブジェクトが変更を行ったことを別のオブジェクトに通知することを可能にします。</span><span class="sxs-lookup"><span data-stu-id="2ed08-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="2ed08-106">変更の種類はイベントと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2ed08-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="2ed08-107">MAPI は、通知が生成されるいくつかのイベントを定義します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="2ed08-108">通常、クライアントは1つまたは複数のオブジェクトを使用して1つ以上のイベントを登録します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="2ed08-109">これらのオブジェクトは、アドバイズソースと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2ed08-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="2ed08-110">アドバイズソースとして機能するオブジェクトには、MAPI のコントロールの下にある session オブジェクト、またはメッセージなどのサービスプロバイダーによって作成されたオブジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="2ed08-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="2ed08-111">通知されたオブジェクトは、アドバイズシンクと呼ばれ、 [IMAPIAdviseSink: iunknown](imapiadvisesinkiunknown.md)インターフェイスまたは[IMAPIViewAdviseSink: iunknown](imapiviewadvisesinkiunknown.md)インターフェイスのいずれかの実装を含み、クライアントアプリケーション内にあります。</span><span class="sxs-lookup"><span data-stu-id="2ed08-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="2ed08-112">アドバイズソースオブジェクト通知を登録するためにクライアントによって呼び出される**アドバイズ**メソッドと、登録をキャンセルするために呼び出される**アドバイズ**中止メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="2ed08-113">**アドバイズ**するパラメーターの1つは、 **IMAPIAdviseSink**または \* \* IMAPIViewAdviseSink \* \* の実装へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="2ed08-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="2ed08-114">アドバイズソースは、変更が発生した場合に、 [IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)または**IMAPIViewAdviseSink**のいずれかのメソッドを呼び出せるように、このポインターをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="2ed08-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="2ed08-115">通知を受信すると、ユーザーは最新の情報を表示できるため、すべてのクライアントが通知を登録して処理することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2ed08-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="2ed08-116">ただし、これは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="2ed08-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="2ed08-117">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="2ed08-117">In this section</span></span>

- <span data-ttu-id="2ed08-118">[通知の登録](registering-for-a-notification.md): 初期化プロセスの一部として、通知のクライアントを登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="2ed08-119">[通知のキャンセル](canceling-a-notification.md): 通知のサブスクリプションを取り消す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="2ed08-120">[メッセージストア通知の処理](handling-message-store-notification.md): メッセージストア通知の登録方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="2ed08-121">[アドレス帳通知](handing-address-book-notification.md)の処理: アドレス帳の通知を登録して処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="2ed08-122">[テーブル通知の処理](handling-table-notification.md): 階層テーブルから通知を登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="2ed08-123">[アドバイズシンクオブジェクトの実装](implementing-an-advise-sink-object.md): アドバイズシンクオブジェクトを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="2ed08-124">[通知のタイミング](timing-a-notification.md): サービスプロバイダーによるクライアント通知のタイミングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="2ed08-125">[スレッドセーフ通知の確認](ensuring-a-thread-safe-notification.md): MAPI を使用してスレッドセーフな通知を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="2ed08-126">[通知の強制](forcing-a-notification.md): MAPI で通知を強制する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ed08-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

