---
title: 通知の登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5a35add66fb685b3c17464269456edf6b456711e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570213"
---
# <a name="registering-for-a-notification"></a><span data-ttu-id="f85d5-103">通知の登録</span><span class="sxs-lookup"><span data-stu-id="f85d5-103">Registering for a Notification</span></span>

  
  
<span data-ttu-id="f85d5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f85d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f85d5-105">クライアントは、その初期化プロセスの一部としてアドレス帳またはメッセージ ストアの通知を登録できます。</span><span class="sxs-lookup"><span data-stu-id="f85d5-105">A client can register for address book or message store notifications as part of its initialization process.</span></span>
  
<span data-ttu-id="f85d5-106">MAPI では、[アドレス帳アドレス帳プロバイダーのいずれかのサポートしているかどうかに関係なく通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f85d5-106">MAPI supports notification on the address book regardless of whether any of the address book providers support it.</span></span> <span data-ttu-id="f85d5-107">メッセージ ・ ストアに通知するためのサポートは、特定のメッセージ ストア プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f85d5-107">Support for notification on message stores depends on the particular message store provider.</span></span> <span data-ttu-id="f85d5-108">特定のメッセージ ストア プロバイダーが通知をサポートしているかどうかを確認するのには、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-108">To determine whether a particular message store provider supports notifications, check its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="f85d5-109">メッセージ ・ ストアでは、通知をサポートする場合は、STORE_NOTIFY_OK ビットが設定されます。</span><span class="sxs-lookup"><span data-stu-id="f85d5-109">If the message store supports notifications, the STORE_NOTIFY_OK bit will be set.</span></span> 
  
<span data-ttu-id="f85d5-110">**アドバイズ ソース オブジェクトのメソッド**を呼び出すことによって、通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-110">Register for notifications by calling an advise source object's **Advise** method.</span></span> <span data-ttu-id="f85d5-111">**アドバイズ**を実装する多くのオブジェクトと、クライアントは、さまざまな方法でそれらのオブジェクトに登録できます。</span><span class="sxs-lookup"><span data-stu-id="f85d5-111">Many objects implement **Advise** and clients can register with those objects in a variety of ways.</span></span> 
  
 <span data-ttu-id="f85d5-112">**通知を登録するのには**</span><span class="sxs-lookup"><span data-stu-id="f85d5-112">**To register for a notification**</span></span>
  
1. <span data-ttu-id="f85d5-113">MAPI の作成通知シンク オブジェクトとその参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="f85d5-113">Create a MAPI advise sink object and increment its reference count.</span></span>
    
2. <span data-ttu-id="f85d5-114">適切であれば、元のアドバイズ シンクをラップするアドバイズ シンク オブジェクトを作成する[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出すし、元の通知シンクを解放.</span><span class="sxs-lookup"><span data-stu-id="f85d5-114">If appropriate, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) to create an advise sink object that wraps your original advise sink, then release the original advice sink..</span></span> 
    
3. <span data-ttu-id="f85d5-115">登録を完了するのには以下の**アドバイス**の方法のいずれかを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-115">Call one of the following **Advise** methods to complete the registration:</span></span> 
    
  - <span data-ttu-id="f85d5-116">セッションの通知や、アドレス帳またはメッセージ ストアのオブジェクトに通知を登録するのには[IMAPISession::Advise](imapisession-advise.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-116">Call [IMAPISession::Advise](imapisession-advise.md) to register for session notifications or for notifications on an address book or message store object.</span></span> 
    
  - <span data-ttu-id="f85d5-117">アドレス帳の通知やメッセージのユーザー、コンテナー、または配布リストに通知を登録するのには[IAddrBook::Advise](iaddrbook-advise.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-117">Call [IAddrBook::Advise](iaddrbook-advise.md) to register for address book notifications or for notifications on a messaging user, container, or distribution list.</span></span> 
    
  - <span data-ttu-id="f85d5-118">通知メッセージのユーザー、コンテナー、または配布リストのアドレス帳プロバイダーを直接登録するのには[IABLogon::Advise](iablogon-advise.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-118">Call [IABLogon::Advise](iablogon-advise.md) to register directly with an address book provider for notifications on a messaging user, container, or distribution list.</span></span> 
    
  - <span data-ttu-id="f85d5-119">メッセージ ストアの通知、フォルダーまたはメッセージの通知を登録するのには[IMsgStore::Advise](imsgstore-advise.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-119">Call [IMsgStore::Advise](imsgstore-advise.md) to register for message store notifications or for notifications on a folder or message.</span></span> 
    
  - <span data-ttu-id="f85d5-120">フォルダーまたはメッセージの通知のメッセージ ストア プロバイダーを直接登録するのには[IMSLogon::Advise](imslogon-advise.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-120">Call [IMSLogon::Advise](imslogon-advise.md) to register directly with a message store provider for notifications on a folder or message.</span></span> 
    
  - <span data-ttu-id="f85d5-121">テーブルの通知を登録するのには[IMAPITable::Advise](imapitable-advise.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-121">Call [IMAPITable::Advise](imapitable-advise.md) to register for table notifications.</span></span> 
    
4. <span data-ttu-id="f85d5-122">**アドバイズ**から返される接続数をキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="f85d5-122">Cache the connection number returned from **Advise**.</span></span>
    
5. <span data-ttu-id="f85d5-123">ラップされたアドバイズ シンクを使用している場合を解放します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-123">If using a wrapped advise sink, release it.</span></span> <span data-ttu-id="f85d5-124">ラップされたアドバイズ シンクが登録されると、不要にします。</span><span class="sxs-lookup"><span data-stu-id="f85d5-124">Once the wrapped advise sink is registered, you no longer need it.</span></span>
    
<span data-ttu-id="f85d5-125">呼び出す * * IMAPISession::Advise * * を使用すると、セッション全体に重大なエラーの通知や個々 のオブジェクトに対してさまざまな通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-125">Calling ** IMAPISession::Advise ** enables you to register for critical error notifications on the overall session or for various notifications on individual objects.</span></span> <span data-ttu-id="f85d5-126">セッションは、共有セッションを使用して別のクライアントが、 [IMAPISession::Logoff](imapisession-logoff.md)メソッドを呼び出すと、共有セッションにログオンするクライアントへの重大なエラーの通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-126">Sessions send critical error notifications to clients logged on to shared sessions when another client using the shared session calls the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> <span data-ttu-id="f85d5-127">セッションの通知を登録するには、エントリの識別子パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-127">To register for session notifications, pass NULL for the entry identifier parameter.</span></span> <span data-ttu-id="f85d5-128">個々 のオブジェクトに通知を登録するには、オブジェクトのエントリ id を渡します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-128">To register for notifications on an individual object, pass the object's entry identifier.</span></span> <span data-ttu-id="f85d5-129">エントリ id の**MAPIUID**の部分で、 **IMAPISession**メソッドは、適切なサービス プロバイダーへの呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-129">The **IMAPISession** method forwards the call to the appropriate service provider, as determined by the **MAPIUID** portion of the entry identifier.</span></span> <span data-ttu-id="f85d5-130">オブジェクトの通知を登録するのには**IMAPISession::Advise**の呼び出しは、**サービス プロバイダーのメソッド**を呼び出すよりも簡単です。</span><span class="sxs-lookup"><span data-stu-id="f85d5-130">Calling **IMAPISession::Advise** to register for object notifications is simpler than calling a service provider's **Advise** method.</span></span> 
  
<span data-ttu-id="f85d5-131">アドレス帳に登録することは、セッションへの登録に似ています。</span><span class="sxs-lookup"><span data-stu-id="f85d5-131">Registering with the address book is similar to registering with the session.</span></span> <span data-ttu-id="f85d5-132">アドレス帳からの重大なエラーの通知を登録するには、エントリの識別子は NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-132">To register for critical error notification from the address book, pass NULL for the entry identifier.</span></span> <span data-ttu-id="f85d5-133">特定のアドレス帳のオブジェクトに通知を登録するには、適切なエントリ id とイベント、または関心のあるイベントを指定します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-133">To register for notifications on a particular address book object, specify the appropriate entry identifier and event or events of interest.</span></span> <span data-ttu-id="f85d5-134">アドレス帳プロバイダーの多くが個々 のオブジェクト上での通知をサポートしていないことに注意します。</span><span class="sxs-lookup"><span data-stu-id="f85d5-134">Be aware that many address book providers do not support notifications on individual objects.</span></span> <span data-ttu-id="f85d5-135">代わりに、その内容および階層テーブルのテーブルの通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f85d5-135">Rather, they support table notifications on their contents and hierarchy tables.</span></span> 
  
<span data-ttu-id="f85d5-136">アドバイズ シンクを実装または**アドバイス**の呼び出しから正常に戻った後すぐに[HrAllocAdviseSink](hrallocadvisesink.md)を作成することを解放することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f85d5-136">It is good practice to release the advise sink that you implement or create with [HrAllocAdviseSink](hrallocadvisesink.md) immediately after a successful return from an **Advise** call.</span></span> <span data-ttu-id="f85d5-137">**アドバイス**の呼び出しの後、アドバイズ シンクをリリースするサービス プロバイダーが、 **Unadvise**の前に呼び出しが行われるためにです。</span><span class="sxs-lookup"><span data-stu-id="f85d5-137">This is because it is possible for service providers to release your advise sink after the **Advise** call, but before an **Unadvise** call is made.</span></span> <span data-ttu-id="f85d5-138">与えたアドバイスのソースのポインター、アドバイズ シンクに、このアドバイズ シンク上で参照カウントがインクリメントされたが、長期的に使用がない限り、それを解放することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f85d5-138">Once you have given the advise source a pointer to your advise sink and the reference count has been incremented on this advise sink, it is wise to release it unless you have a long term use for it.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f85d5-139">**Unadvise**の呼び出しが行われるまで、すべての接続番号を表す有効な勧告の登録は解除できません。</span><span class="sxs-lookup"><span data-stu-id="f85d5-139">All connection numbers that represent valid advisory registrations will not be released until the **Unadvise** call is made.</span></span> 
  

