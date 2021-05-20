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
# <a name="handling-notifications"></a><span data-ttu-id="3a426-103">通知の処理</span><span class="sxs-lookup"><span data-stu-id="3a426-103">Handling notifications</span></span>

<span data-ttu-id="3a426-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a426-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a426-105">通知を使用すると、あるオブジェクトが変更を受けたことを別のオブジェクトに通知できます。</span><span class="sxs-lookup"><span data-stu-id="3a426-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="3a426-106">変更の種類はイベントと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="3a426-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="3a426-107">MAPI は、通知が生成されるいくつかのイベントを定義します。</span><span class="sxs-lookup"><span data-stu-id="3a426-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="3a426-108">クライアントは通常、1 つ以上のオブジェクトを持つ 1 つ以上のイベントに登録します。</span><span class="sxs-lookup"><span data-stu-id="3a426-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="3a426-109">これらのオブジェクトは、アドバイス ソースと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="3a426-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="3a426-110">アドバイス ソースとして機能できるオブジェクトには、セッション オブジェクト、MAPI のコントロールの下、またはメッセージなどのサービス プロバイダーによって作成されたオブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3a426-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="3a426-111">通知シンクと呼ばれる情報に基づいたオブジェクトには [、IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) インターフェイスまたは [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) インターフェイスの実装が含まれているので、クライアント アプリケーション内に格納されます。</span><span class="sxs-lookup"><span data-stu-id="3a426-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="3a426-112">アドバイス ソース オブジェクトは **、通知** を登録するためにクライアントによって呼び出される Advise メソッドと、登録をキャンセルするために呼び出される **Unadvise** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="3a426-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="3a426-113">Advise のパラメーターの **1** つは **、IMAPIAdviseSink** または \*\* IMAPIViewAdviseSink \*\*の実装へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="3a426-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="3a426-114">変更が発生すると、このポインターは [、IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) または **IMAPIViewAdviseSink** のいずれかのメソッドを呼び出す際に、このポインターをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="3a426-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="3a426-115">通知を受信すると、ユーザーは最新の情報を表示することができますので、すべてのクライアントが通知に登録して処理を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a426-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="3a426-116">ただし、省略可能です。</span><span class="sxs-lookup"><span data-stu-id="3a426-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="3a426-117">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="3a426-117">In this section</span></span>

- <span data-ttu-id="3a426-118">[通知の登録](registering-for-a-notification.md): クライアントを初期化プロセスの一部として通知に登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="3a426-119">[通知のキャンセル](canceling-a-notification.md): 通知へのサブスクリプションをキャンセルする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="3a426-120">[メッセージ ストア通知の処理](handling-message-store-notification.md): メッセージ ストア通知に登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="3a426-121">[[アドレス帳の通知を渡す](handing-address-book-notification.md)]: アドレス帳の通知を登録して処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="3a426-122">[テーブル通知の処理](handling-table-notification.md): 階層テーブルからの通知を登録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="3a426-123">[Advise Sink オブジェクトの実装](implementing-an-advise-sink-object.md): アアドバイス シンク オブジェクトを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="3a426-124">[通知のタイミング](timing-a-notification.md): サービス プロバイダーによるクライアント通知のタイミングについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="3a426-125">[[通知のThread-Safeする](ensuring-a-thread-safe-notification.md): MAPI を使用してスレッド セーフ通知を確認する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="3a426-126">[通知の強制](forcing-a-notification.md): MAPI で通知を強制する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a426-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

