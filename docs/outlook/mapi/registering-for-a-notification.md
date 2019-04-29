---
title: 通知の登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 45625387-dbd2-4ca8-926b-ef87998d01d7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ccc2758b59a9227afbc50360102e793892bbdc52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424904"
---
# <a name="registering-for-a-notification"></a><span data-ttu-id="1ec5e-103">通知の登録</span><span class="sxs-lookup"><span data-stu-id="1ec5e-103">Registering for a Notification</span></span>

  
  
<span data-ttu-id="1ec5e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ec5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ec5e-105">クライアントは、初期化プロセスの一環として、アドレス帳またはメッセージストア通知の登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-105">A client can register for address book or message store notifications as part of its initialization process.</span></span>
  
<span data-ttu-id="1ec5e-106">MAPI は、アドレス帳プロバイダーがサポートしているかどうかに関係なく、アドレス帳での通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-106">MAPI supports notification on the address book regardless of whether any of the address book providers support it.</span></span> <span data-ttu-id="1ec5e-107">メッセージストアに対する通知のサポートは、特定のメッセージストアプロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-107">Support for notification on message stores depends on the particular message store provider.</span></span> <span data-ttu-id="1ec5e-108">特定のメッセージストアプロバイダーが通知をサポートしているかどうかを判断するには、その**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-108">To determine whether a particular message store provider supports notifications, check its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="1ec5e-109">メッセージストアが通知をサポートしている場合は、STORE_NOTIFY_OK ビットが設定されます。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-109">If the message store supports notifications, the STORE_NOTIFY_OK bit will be set.</span></span> 
  
<span data-ttu-id="1ec5e-110">アドバイズソースオブジェクトの**アドバイズ**メソッドを呼び出して通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-110">Register for notifications by calling an advise source object's **Advise** method.</span></span> <span data-ttu-id="1ec5e-111">多くのオブジェクトは**アドバイズ**を実装し、クライアントはさまざまな方法でそれらのオブジェクトに登録できます。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-111">Many objects implement **Advise** and clients can register with those objects in a variety of ways.</span></span> 
  
 <span data-ttu-id="1ec5e-112">**通知を登録するには**</span><span class="sxs-lookup"><span data-stu-id="1ec5e-112">**To register for a notification**</span></span>
  
1. <span data-ttu-id="1ec5e-113">MAPI アドバイズシンクオブジェクトを作成し、その参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-113">Create a MAPI advise sink object and increment its reference count.</span></span>
    
2. <span data-ttu-id="1ec5e-114">必要に応じて、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)を呼び出して、元のアドバイズシンクをラップするアドバイズシンクオブジェクトを作成し、元の通知シンクを解放します。.</span><span class="sxs-lookup"><span data-stu-id="1ec5e-114">If appropriate, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) to create an advise sink object that wraps your original advise sink, then release the original advice sink..</span></span> 
    
3. <span data-ttu-id="1ec5e-115">登録を完了するには、次のいずれかの**アドバイズ**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-115">Call one of the following **Advise** methods to complete the registration:</span></span> 
    
  - <span data-ttu-id="1ec5e-116">呼び出し[imapisession::](imapisession-advise.md)セッション通知の登録またはアドレス帳またはメッセージストアオブジェクトの通知のための通知。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-116">Call [IMAPISession::Advise](imapisession-advise.md) to register for session notifications or for notifications on an address book or message store object.</span></span> 
    
  - <span data-ttu-id="1ec5e-117">Call [IAddrBook::](iaddrbook-advise.md)アドレス帳通知の登録、またはメッセージングユーザー、コンテナー、または配布リストでの通知についてアドバイスを行います。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-117">Call [IAddrBook::Advise](iaddrbook-advise.md) to register for address book notifications or for notifications on a messaging user, container, or distribution list.</span></span> 
    
  - <span data-ttu-id="1ec5e-118">Call [IABLogon::](iablogon-advise.md)通知のユーザー、コンテナー、または配布リストに通知するために、アドレス帳プロバイダーに直接登録するようにアドバイスします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-118">Call [IABLogon::Advise](iablogon-advise.md) to register directly with an address book provider for notifications on a messaging user, container, or distribution list.</span></span> 
    
  - <span data-ttu-id="1ec5e-119">Call [IMsgStore::](imsgstore-advise.md)メッセージストア通知またはフォルダーまたはメッセージの通知を登録するようにアドバイスします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-119">Call [IMsgStore::Advise](imsgstore-advise.md) to register for message store notifications or for notifications on a folder or message.</span></span> 
    
  - <span data-ttu-id="1ec5e-120">[IMSLogon:: アドバイス](imslogon-advise.md)を呼び出して、フォルダーまたはメッセージに通知するメッセージストアプロバイダーを直接登録します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-120">Call [IMSLogon::Advise](imslogon-advise.md) to register directly with a message store provider for notifications on a folder or message.</span></span> 
    
  - <span data-ttu-id="1ec5e-121">呼び出し[IMAPITable:: アドバイス](imapitable-advise.md)を表通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-121">Call [IMAPITable::Advise](imapitable-advise.md) to register for table notifications.</span></span> 
    
4. <span data-ttu-id="1ec5e-122">Cache**アドバイズ**から返される接続番号をキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-122">Cache the connection number returned from **Advise**.</span></span>
    
5. <span data-ttu-id="1ec5e-123">ラップされたアドバイズシンクを使用している場合は、それをリリースします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-123">If using a wrapped advise sink, release it.</span></span> <span data-ttu-id="1ec5e-124">ラップされたアドバイズシンクが登録されると、必要なくなります。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-124">Once the wrapped advise sink is registered, you no longer need it.</span></span>
    
<span data-ttu-id="1ec5e-125">呼び出し \* \* imapisession:: Advise \* \* は、セッション全体または個々のオブジェクトに関するさまざまな通知に関する重大なエラー通知の登録を可能にします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-125">Calling \*\* IMAPISession::Advise \*\* enables you to register for critical error notifications on the overall session or for various notifications on individual objects.</span></span> <span data-ttu-id="1ec5e-126">セッションは、共有セッションを使用している別のクライアントが[imapisession:: Logoff](imapisession-logoff.md)メソッドを呼び出すときに、共有セッションにログオンしているクライアントに重大なエラー通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-126">Sessions send critical error notifications to clients logged on to shared sessions when another client using the shared session calls the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> <span data-ttu-id="1ec5e-127">セッション通知を登録するには、エントリ識別子パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-127">To register for session notifications, pass NULL for the entry identifier parameter.</span></span> <span data-ttu-id="1ec5e-128">個々のオブジェクトの通知を登録するには、オブジェクトのエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-128">To register for notifications on an individual object, pass the object's entry identifier.</span></span> <span data-ttu-id="1ec5e-129">**imapisession**メソッドは、エントリ識別子の**MAPIUID**部分に基づいて、適切なサービスプロバイダーに呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-129">The **IMAPISession** method forwards the call to the appropriate service provider, as determined by the **MAPIUID** portion of the entry identifier.</span></span> <span data-ttu-id="1ec5e-130">**imapisession:: アドバイス**をオブジェクト通知に登録することは、サービスプロバイダーの**アドバイズ**メソッドを呼び出すよりも簡単です。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-130">Calling **IMAPISession::Advise** to register for object notifications is simpler than calling a service provider's **Advise** method.</span></span> 
  
<span data-ttu-id="1ec5e-131">アドレス帳を使用して登録することは、セッションに登録するのと似ています。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-131">Registering with the address book is similar to registering with the session.</span></span> <span data-ttu-id="1ec5e-132">アドレス帳から重大なエラー通知を登録するには、エントリ識別子に NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-132">To register for critical error notification from the address book, pass NULL for the entry identifier.</span></span> <span data-ttu-id="1ec5e-133">特定のアドレス帳オブジェクトで通知を登録するには、適切なエントリ識別子とイベントを指定します。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-133">To register for notifications on a particular address book object, specify the appropriate entry identifier and event or events of interest.</span></span> <span data-ttu-id="1ec5e-134">多くのアドレス帳プロバイダーは、個々のオブジェクトに対する通知をサポートしていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-134">Be aware that many address book providers do not support notifications on individual objects.</span></span> <span data-ttu-id="1ec5e-135">その代わりに、コンテンツおよび階層テーブルのテーブル通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-135">Rather, they support table notifications on their contents and hierarchy tables.</span></span> 
  
<span data-ttu-id="1ec5e-136">**アドバイズ**呼び出しから正常に復帰した直後に、 [HrAllocAdviseSink](hrallocadvisesink.md)で実装または作成したアドバイズシンクを解放することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-136">It is good practice to release the advise sink that you implement or create with [HrAllocAdviseSink](hrallocadvisesink.md) immediately after a successful return from an **Advise** call.</span></span> <span data-ttu-id="1ec5e-137">これは、サービスプロバイダーがアドバイズ呼び出しの後、アドバイズ中止呼び出しが行わ\*\*\*\* れる前に、アドバイズシンク\*\*\*\* を解放できるためです。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-137">This is because it is possible for service providers to release your advise sink after the **Advise** call, but before an **Unadvise** call is made.</span></span> <span data-ttu-id="1ec5e-138">アドバイズソースがアドバイズシンクへのポインターを取得し、このアドバイズシンクで参照カウントがインクリメントされたら、長期に使用していない限り、リリースすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-138">Once you have given the advise source a pointer to your advise sink and the reference count has been incremented on this advise sink, it is wise to release it unless you have a long term use for it.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1ec5e-139">有効なアドバイザリの登録を表すすべての接続番号は、**アドバイズ**中止の呼び出しが行われるまで解放されません。</span><span class="sxs-lookup"><span data-stu-id="1ec5e-139">All connection numbers that represent valid advisory registrations will not be released until the **Unadvise** call is made.</span></span> 
  

