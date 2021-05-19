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
# <a name="registering-for-a-notification"></a><span data-ttu-id="42a8c-103">通知の登録</span><span class="sxs-lookup"><span data-stu-id="42a8c-103">Registering for a Notification</span></span>

  
  
<span data-ttu-id="42a8c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42a8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42a8c-105">クライアントは、初期化プロセスの一環としてアドレス帳またはメッセージ ストア通知に登録できます。</span><span class="sxs-lookup"><span data-stu-id="42a8c-105">A client can register for address book or message store notifications as part of its initialization process.</span></span>
  
<span data-ttu-id="42a8c-106">MAPI は、アドレス帳プロバイダーがサポートするかどうかに関係なく、アドレス帳の通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="42a8c-106">MAPI supports notification on the address book regardless of whether any of the address book providers support it.</span></span> <span data-ttu-id="42a8c-107">メッセージ ストアでの通知のサポートは、特定のメッセージ ストア プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="42a8c-107">Support for notification on message stores depends on the particular message store provider.</span></span> <span data-ttu-id="42a8c-108">特定のメッセージ ストア プロバイダーが通知をサポートするかどうかを確認するには、PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-108">To determine whether a particular message store provider supports notifications, check its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> <span data-ttu-id="42a8c-109">メッセージ ストアで通知がサポートされている場合、STORE_NOTIFY_OKビットが設定されます。</span><span class="sxs-lookup"><span data-stu-id="42a8c-109">If the message store supports notifications, the STORE_NOTIFY_OK bit will be set.</span></span> 
  
<span data-ttu-id="42a8c-110">アドバイス ソース オブジェクトの Advise メソッドを呼び出して通知に **登録** します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-110">Register for notifications by calling an advise source object's **Advise** method.</span></span> <span data-ttu-id="42a8c-111">多くのオブジェクトは **Advise** を実装し、クライアントはさまざまな方法でこれらのオブジェクトに登録できます。</span><span class="sxs-lookup"><span data-stu-id="42a8c-111">Many objects implement **Advise** and clients can register with those objects in a variety of ways.</span></span> 
  
 <span data-ttu-id="42a8c-112">**通知に登録するには**</span><span class="sxs-lookup"><span data-stu-id="42a8c-112">**To register for a notification**</span></span>
  
1. <span data-ttu-id="42a8c-113">MAPI アアドバイス シンク オブジェクトを作成し、その参照カウントを増やします。</span><span class="sxs-lookup"><span data-stu-id="42a8c-113">Create a MAPI advise sink object and increment its reference count.</span></span>
    
2. <span data-ttu-id="42a8c-114">必要に応じて [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md) を呼び出して、元のアアドバイス シンクをラップするアアドバイス シンク オブジェクトを作成し、元のアドバイス シンクを解放します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-114">If appropriate, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) to create an advise sink object that wraps your original advise sink, then release the original advice sink..</span></span> 
    
3. <span data-ttu-id="42a8c-115">登録を完了するには、次 **のいずれかの Advise** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-115">Call one of the following **Advise** methods to complete the registration:</span></span> 
    
  - <span data-ttu-id="42a8c-116">[IMAPISession::通知](imapisession-advise.md)を呼び出して、セッション通知またはアドレス帳またはメッセージ ストア オブジェクトの通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-116">Call [IMAPISession::Advise](imapisession-advise.md) to register for session notifications or for notifications on an address book or message store object.</span></span> 
    
  - <span data-ttu-id="42a8c-117">[IAddrBook::Advise を](iaddrbook-advise.md)呼び出して、アドレス帳通知またはメッセージング ユーザー、コンテナー、または配布リストの通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-117">Call [IAddrBook::Advise](iaddrbook-advise.md) to register for address book notifications or for notifications on a messaging user, container, or distribution list.</span></span> 
    
  - <span data-ttu-id="42a8c-118">[IABLogon::Advise](iablogon-advise.md)を呼び出して、メッセージング ユーザー、コンテナー、または配布リストの通知をアドレス帳プロバイダーに直接登録します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-118">Call [IABLogon::Advise](iablogon-advise.md) to register directly with an address book provider for notifications on a messaging user, container, or distribution list.</span></span> 
    
  - <span data-ttu-id="42a8c-119">[IMsgStore::Advise を](imsgstore-advise.md)呼び出して、メッセージ ストア通知またはフォルダーまたはメッセージの通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-119">Call [IMsgStore::Advise](imsgstore-advise.md) to register for message store notifications or for notifications on a folder or message.</span></span> 
    
  - <span data-ttu-id="42a8c-120">[IMSLogon::Advise を](imslogon-advise.md)呼び出して、フォルダーまたはメッセージの通知をメッセージ ストア プロバイダーに直接登録します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-120">Call [IMSLogon::Advise](imslogon-advise.md) to register directly with a message store provider for notifications on a folder or message.</span></span> 
    
  - <span data-ttu-id="42a8c-121">[IMAPITable::Advise を呼び出して、](imapitable-advise.md)テーブル通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-121">Call [IMAPITable::Advise](imapitable-advise.md) to register for table notifications.</span></span> 
    
4. <span data-ttu-id="42a8c-122">Advise から返される接続番号を **キャッシュします**。</span><span class="sxs-lookup"><span data-stu-id="42a8c-122">Cache the connection number returned from **Advise**.</span></span>
    
5. <span data-ttu-id="42a8c-123">ラップされたアアドバイス シンクを使用する場合は、リリースします。</span><span class="sxs-lookup"><span data-stu-id="42a8c-123">If using a wrapped advise sink, release it.</span></span> <span data-ttu-id="42a8c-124">ラップされたアアドバイス シンクが登録された後、そのシンクは不要です。</span><span class="sxs-lookup"><span data-stu-id="42a8c-124">Once the wrapped advise sink is registered, you no longer need it.</span></span>
    
<span data-ttu-id="42a8c-125">呼び出し \*\* IMAPISession::Advise \*\* を使用すると、セッション全体または個々のオブジェクトに対するさまざまな通知に対して重大なエラー通知を登録できます。</span><span class="sxs-lookup"><span data-stu-id="42a8c-125">Calling \*\* IMAPISession::Advise \*\* enables you to register for critical error notifications on the overall session or for various notifications on individual objects.</span></span> <span data-ttu-id="42a8c-126">共有セッションを使用している別のクライアントが [IMAPISession::Logoff](imapisession-logoff.md) メソッドを呼び出す場合、セッションは共有セッションにログオンしているクライアントに重大なエラー通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-126">Sessions send critical error notifications to clients logged on to shared sessions when another client using the shared session calls the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> <span data-ttu-id="42a8c-127">セッション通知に登録するには、エントリ識別子パラメーターに NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-127">To register for session notifications, pass NULL for the entry identifier parameter.</span></span> <span data-ttu-id="42a8c-128">個々のオブジェクトの通知に登録するには、オブジェクトのエントリ識別子を渡します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-128">To register for notifications on an individual object, pass the object's entry identifier.</span></span> <span data-ttu-id="42a8c-129">**IMAPISession** メソッドは、エントリ識別子の **MAPIUID** 部分によって決定される適切なサービス プロバイダーに呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-129">The **IMAPISession** method forwards the call to the appropriate service provider, as determined by the **MAPIUID** portion of the entry identifier.</span></span> <span data-ttu-id="42a8c-130">**IMAPISession::Advise を** 呼び出して、オブジェクト通知に登録する方が、サービス プロバイダーの Advise メソッドを呼び出すよりも **簡単** です。</span><span class="sxs-lookup"><span data-stu-id="42a8c-130">Calling **IMAPISession::Advise** to register for object notifications is simpler than calling a service provider's **Advise** method.</span></span> 
  
<span data-ttu-id="42a8c-131">アドレス帳への登録は、セッションへの登録に似ています。</span><span class="sxs-lookup"><span data-stu-id="42a8c-131">Registering with the address book is similar to registering with the session.</span></span> <span data-ttu-id="42a8c-132">アドレス帳から重大なエラー通知を登録するには、エントリ識別子に NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-132">To register for critical error notification from the address book, pass NULL for the entry identifier.</span></span> <span data-ttu-id="42a8c-133">特定のアドレス帳オブジェクトに通知を登録するには、適切なエントリ識別子と、対象のイベントまたはイベントを指定します。</span><span class="sxs-lookup"><span data-stu-id="42a8c-133">To register for notifications on a particular address book object, specify the appropriate entry identifier and event or events of interest.</span></span> <span data-ttu-id="42a8c-134">アドレス帳プロバイダーの多くは、個々のオブジェクトに対する通知をサポートしていない点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="42a8c-134">Be aware that many address book providers do not support notifications on individual objects.</span></span> <span data-ttu-id="42a8c-135">むしろ、コンテンツテーブルと階層テーブルに対するテーブル通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="42a8c-135">Rather, they support table notifications on their contents and hierarchy tables.</span></span> 
  
<span data-ttu-id="42a8c-136">アドバイスの呼び出しから正常に戻った直後に[、HrAllocAdviseSink](hrallocadvisesink.md)を使用して実装または作成するアドバイス シンクを解放してください。</span><span class="sxs-lookup"><span data-stu-id="42a8c-136">It is good practice to release the advise sink that you implement or create with [HrAllocAdviseSink](hrallocadvisesink.md) immediately after a successful return from an **Advise** call.</span></span> <span data-ttu-id="42a8c-137">これは、サービス プロバイダーが、 **アドバイス** の呼び出し後 **、Unadvise** 呼び出しが行われた前にアアドバイス シンクを解放できる可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="42a8c-137">This is because it is possible for service providers to release your advise sink after the **Advise** call, but before an **Unadvise** call is made.</span></span> <span data-ttu-id="42a8c-138">アドバイス ソースにアアドバイス シンクへのポインターを指定し、このアアドバイス シンクで参照カウントを増やしたら、長期的な使用がない限り、それを解放する方が賢明です。</span><span class="sxs-lookup"><span data-stu-id="42a8c-138">Once you have given the advise source a pointer to your advise sink and the reference count has been incremented on this advise sink, it is wise to release it unless you have a long term use for it.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="42a8c-139">有効なアドバイザリ登録を表すすべての接続番号は **、Unadvise** 呼び出しが行われたまで解放されません。</span><span class="sxs-lookup"><span data-stu-id="42a8c-139">All connection numbers that represent valid advisory registrations will not be released until the **Unadvise** call is made.</span></span> 
  

