---
title: 通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4c19e88ac1cfb29a9841ec78516410e23b3e5403
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567581"
---
# <a name="handling-notifications"></a><span data-ttu-id="f3602-103">通知の処理</span><span class="sxs-lookup"><span data-stu-id="f3602-103">Handling notifications</span></span>

<span data-ttu-id="f3602-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3602-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3602-105">通知が別に通知する 1 つのオブジェクトを有効にするオブジェクトの変更が行われています。</span><span class="sxs-lookup"><span data-stu-id="f3602-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="f3602-106">変更の種類は、"イベント"と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f3602-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="f3602-107">MAPI では、通知を生成するいくつかのイベントを定義します。</span><span class="sxs-lookup"><span data-stu-id="f3602-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="f3602-108">クライアントは、通常 1 つまたは複数のオブジェクトを 1 つまたは複数のイベントを登録します。</span><span class="sxs-lookup"><span data-stu-id="f3602-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="f3602-109">これらのオブジェクトは、ソースの通知と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f3602-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="f3602-110">通知ソースとして機能するオブジェクトには、MAPI のコントロール、またはメッセージなどのサービス プロバイダーによって作成されたオブジェクトの下にある、セッション オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3602-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="f3602-111">、アドバイズ シンクと呼ばれる、オブジェクト情報を入手するには、いずれかの実装が含まれています、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インタ フェース、または[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インタ フェースし、クライアント アプリケーション内にあります。</span><span class="sxs-lookup"><span data-stu-id="f3602-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="f3602-112">アドバイズ ソース オブジェクトは、**アドバイズ**メソッドは、通知を登録するクライアントによって呼び出されると、登録をキャンセルすると呼ばれる**Unadvise**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="f3602-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="f3602-113">**アドバイズ**するパラメーターの 1 つは、 **IMAPIAdviseSink**の実装へのポインターまたは * * IMAPIViewAdviseSink * * です。</span><span class="sxs-lookup"><span data-stu-id="f3602-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or ** IMAPIViewAdviseSink **.</span></span> <span data-ttu-id="f3602-114">呼び出すことが[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)またはのいずれかの**IMAPIViewAdviseSink**に変更が発生したときにできるように、アドバイスのソースはこのポインターをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="f3602-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="f3602-115">通知を受信できるように、最新の情報を表示するのには、ために、すべてのクライアントを登録し、通知の処理をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f3602-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="f3602-116">ただし、省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f3602-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="f3602-117">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="f3602-117">In this section</span></span>

- <span data-ttu-id="f3602-118">[通知を登録する](registering-for-a-notification.md): その初期化プロセスの一部としてクライアントの通知を登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="f3602-119">[通知をキャンセルする](canceling-a-notification.md): 通知に対するサブスクリプションをキャンセルする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="f3602-120">[メッセージ保存通知の処理](handling-message-store-notification.md): メッセージ ストアの通知を登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="f3602-121">[アドレス帳の通知の処理](handing-address-book-notification.md): 登録し、アドレス帳の通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="f3602-122">[テーブル通知の処理](handling-table-notification.md): 階層テーブルからの通知を登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="f3602-123">[通知シンク オブジェクトを実装する](implementing-an-advise-sink-object.md): アドバイズ シンク オブジェクトを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="f3602-124">[通知のタイミング](timing-a-notification.md): サービス プロバイダーによってクライアントへの通知のタイミングを説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="f3602-125">[通知スレッド セーフを確保する](ensuring-a-thread-safe-notification.md): MAPI の通知をスレッド セーフであることを確認する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="f3602-126">[強制的に通知](forcing-a-notification.md): mapi 通知を強制する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f3602-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

