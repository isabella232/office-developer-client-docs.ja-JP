---
title: MAPI のスレッド処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405542"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="6e9a0-103">MAPI のスレッド処理</span><span class="sxs-lookup"><span data-stu-id="6e9a0-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="6e9a0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e9a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e9a0-105">スレッドは、オペレーティング システムが CPU 時間を割り当てる基本的なエンティティです。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="6e9a0-106">スレッドには独自のレジスタ、スタック、優先度、ストレージがありますが、アドレス空間とアクセス トークンなどのプロセス リソースを共有します。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="6e9a0-107">スレッドはメモリも共有し、1 つのスレッドが別のスレッドが書き込んだ値を読み取っています。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="6e9a0-108">MAPI クライアントは、次の汎用スレッド モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="6e9a0-109">**スレッド モデル**</span><span class="sxs-lookup"><span data-stu-id="6e9a0-109">**Threading model**</span></span>|<span data-ttu-id="6e9a0-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="6e9a0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e9a0-111">シングル スレッド モデル</span><span class="sxs-lookup"><span data-stu-id="6e9a0-111">Single threading model</span></span>  <br/> |<span data-ttu-id="6e9a0-112">すべてのオブジェクトは、単一スレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="6e9a0-113">アパートメント スレッド モデル</span><span class="sxs-lookup"><span data-stu-id="6e9a0-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="6e9a0-114">オブジェクトは、オブジェクトを作成したスレッドでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="6e9a0-115">フリー スレッド(スレッド パーティ)モデル</span><span class="sxs-lookup"><span data-stu-id="6e9a0-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="6e9a0-116">オブジェクトは、任意のスレッドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="6e9a0-117">MAPI は、任意のスレッドでいつでも使用できるスレッド セーフ オブジェクトをサポートする、無料のスレッド モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="6e9a0-118">OLE は、アパートメント スレッド モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="6e9a0-119">アパートメント スレッド モデルは、オブジェクトを作成したスレッド以外のスレッドがオブジェクトを使用する必要がある場合に明示的に転送する必要があるオブジェクトをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="6e9a0-120">OLE がオブジェクトをあるスレッドから別のスレッドに転送するために使用するメカニズムは、マーシャリングと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="6e9a0-121">マーシャリングには、スタブ オブジェクトとプロキシ オブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="6e9a0-122">これらの特別なオブジェクトは、マーシャリングするオブジェクト内のインターフェイスのパラメーターをパッケージ化し、これらのパラメーターを他のスレッドに転送し、到着時に開梱します。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="6e9a0-123">2 つのマルチスレッド モデル間の競合は、OLE "軽量" リモート プロシージャ 呼び出し (LRPC) を使用して、フリー スレッド MAPI オブジェクトが別のプロセスに送信される場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="6e9a0-124">LRPC は、スタブ インターフェイスとプロキシ インターフェイスと、オブジェクトと呼び出し元の間にアパートメント スレッド動作を介在させて、オブジェクトのセマンティクスをフリー スレッドからアパートメント スレッドに変更します。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="6e9a0-125">この競合につながる MAPI の状況を認識すると、クライアントとサービス プロバイダーが問題が発生しなくなります。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="6e9a0-126">MAPI オブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="6e9a0-127">[MAPILogonEx](mapilogonex.md)から返されるセッション オブジェクトなど、クライアントのプロセスにリンクされたサービス プロバイダーまたは MAPI によって返されるインターフェイス ポインターを使用して、メソッドを直接呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="6e9a0-128">[IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)の別のフォルダーからコピーされたフォルダー オブジェクトなど、サービス プロバイダーが返すインターフェイス ポインターを使用して、メソッドへの間接的な呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="6e9a0-129">サービス プロバイダーまたは MAPI に渡される [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドなどのコールバック関数を使用して、 **アドバイス** 呼び出しまたは長い操作の進行状況を表示できるメソッド。</span><span class="sxs-lookup"><span data-stu-id="6e9a0-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

