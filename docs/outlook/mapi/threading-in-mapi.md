---
title: MAPI のスレッド処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d9ee45ea7a3592a2b0fc0675bbdb6e640f9bd046
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580391"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="00ecc-103">MAPI のスレッド処理</span><span class="sxs-lookup"><span data-stu-id="00ecc-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="00ecc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00ecc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00ecc-105">スレッドは、オペレーティング システムが CPU 時間を割り当てる基本的なエンティティです。</span><span class="sxs-lookup"><span data-stu-id="00ecc-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="00ecc-106">スレッド独自のレジスタ、スタック、優先順位、およびストレージがアクセス トークンなどのアドレス領域と処理リソースを共有します。</span><span class="sxs-lookup"><span data-stu-id="00ecc-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="00ecc-107">スレッドは、別のスレッドが書き込まれた内容を読み取り、1 つのスレッドでも、メモリを共有します。</span><span class="sxs-lookup"><span data-stu-id="00ecc-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="00ecc-108">MAPI クライアントでは、次の一般的なスレッド モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="00ecc-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="00ecc-109">**スレッド モデル**</span><span class="sxs-lookup"><span data-stu-id="00ecc-109">**Threading model**</span></span>|<span data-ttu-id="00ecc-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="00ecc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00ecc-111">シングル スレッド モデル</span><span class="sxs-lookup"><span data-stu-id="00ecc-111">Single threading model</span></span>  <br/> |<span data-ttu-id="00ecc-112">すべてのオブジェクトは、単一のスレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="00ecc-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="00ecc-113">アパートメント スレッド モデル</span><span class="sxs-lookup"><span data-stu-id="00ecc-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="00ecc-114">オブジェクトは、作成されたスレッド上でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="00ecc-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="00ecc-115">フリー スレッドまたはスレッドの関係者、モデル</span><span class="sxs-lookup"><span data-stu-id="00ecc-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="00ecc-116">オブジェクトは、任意のスレッドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="00ecc-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="00ecc-117">MAPI では、いつでも任意のスレッドで使用できるスレッド セーフなオブジェクトをサポートするフリー スレッド モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="00ecc-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="00ecc-118">OLE では、アパートメント スレッド モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="00ecc-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="00ecc-119">アパートメント スレッド モデルには、オブジェクト以外のオブジェクトを作成したスレッドがそのオブジェクトを使用する必要がある場合に明示的に転送する必要がありますがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="00ecc-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="00ecc-120">OLE を使用してオブジェクトを別の 1 つのスレッドに転送する機構は、マーシャ リングと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="00ecc-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="00ecc-121">マーシャ リングには、スタブ オブジェクトとプロキシ オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="00ecc-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="00ecc-122">これらの特別なオブジェクトは、マーシャ リングする、これらのパラメーターを他のスレッドに転送および到着時にそれらのパッケージを展開するオブジェクトのインターフェイスのパラメーターをパッケージ化します。</span><span class="sxs-lookup"><span data-stu-id="00ecc-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="00ecc-123">2 つのマルチ スレッド モデル間の衝突は、フリー スレッドの MAPI オブジェクトが OLE「軽量な」リモート プロシージャ コール、または LRPC を使用して別のプロセスに送信されるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="00ecc-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="00ecc-124">LRPC は、アパートメントのスレッド アパートメント スレッド、呼び出し元のオブジェクトとの間での動作を持つスタブとプロキシのインターフェイスを置くことによってするフリー スレッドのオブジェクトのセマンティクスを変更します。</span><span class="sxs-lookup"><span data-stu-id="00ecc-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="00ecc-125">MAPI でのこのような競合の原因となる状況の認識を支援し、サービス ・ プロバイダーの問題の発生を防ぐ。</span><span class="sxs-lookup"><span data-stu-id="00ecc-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="00ecc-126">MAPI オブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="00ecc-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="00ecc-127">インタ フェースを使用してそのメソッドへの直接呼び出しをサービス プロバイダーまたは MAPI によって返されたポインターにリンクされているクライアントのプロセスでは、 [MAPILogonEx](mapilogonex.md)からセッション オブジェクトが返されるようです。</span><span class="sxs-lookup"><span data-stu-id="00ecc-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="00ecc-128">間接的なメソッドをコール、フォルダー オブジェクトなど、任意のサービス プロバイダーによって返されるインターフェイス ポインターを使用して、 [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)の別のフォルダーからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="00ecc-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="00ecc-129">渡されたまたは MAPI サービス プロバイダーに、**アドバイス**の呼び出し、または時間のかかる操作の進行状況を表示することができるメソッド、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドなどのコールバック関数です。</span><span class="sxs-lookup"><span data-stu-id="00ecc-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

