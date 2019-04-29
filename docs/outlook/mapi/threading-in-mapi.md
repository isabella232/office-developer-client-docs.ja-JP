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
# <a name="threading-in-mapi"></a><span data-ttu-id="fa188-103">MAPI のスレッド処理</span><span class="sxs-lookup"><span data-stu-id="fa188-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="fa188-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa188-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa188-105">スレッドとは、オペレーティングシステムが CPU 時間を割り当てる基本的なエンティティです。</span><span class="sxs-lookup"><span data-stu-id="fa188-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="fa188-106">スレッドには、独自のレジスタ、スタック、優先度、および記憶域がありますが、アドレス空間を共有し、アクセストークンなどのリソースを処理します。</span><span class="sxs-lookup"><span data-stu-id="fa188-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="fa188-107">スレッドはメモリを共有し、1つのスレッドが別のスレッドが書き込んだ内容を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="fa188-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="fa188-108">MAPI クライアントでは、次の汎用スレッドモデルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa188-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="fa188-109">**スレッドモデル**</span><span class="sxs-lookup"><span data-stu-id="fa188-109">**Threading model**</span></span>|<span data-ttu-id="fa188-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="fa188-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa188-111">単一スレッドモデル</span><span class="sxs-lookup"><span data-stu-id="fa188-111">Single threading model</span></span>  <br/> |<span data-ttu-id="fa188-112">すべてのオブジェクトは、1つのスレッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa188-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="fa188-113">アパートメントスレッドモデル</span><span class="sxs-lookup"><span data-stu-id="fa188-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="fa188-114">オブジェクトは、それを作成したスレッドでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa188-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="fa188-115">フリースレッドまたはスレッドパーティ、モデル</span><span class="sxs-lookup"><span data-stu-id="fa188-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="fa188-116">オブジェクトは任意のスレッドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa188-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="fa188-117">MAPI では、任意のスレッドでいつでも使用できるスレッドセーフなオブジェクトをサポートする、フリースレッドモデルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa188-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="fa188-118">OLE はアパートメントスレッドモデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa188-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="fa188-119">アパートメントスレッドモデルでは、オブジェクトを作成したスレッド以外のスレッドがそのオブジェクトを使用する必要がある場合に、明示的に転送する必要があるオブジェクトをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="fa188-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="fa188-120">OLE がオブジェクトを別のスレッドに転送する際に使用するメカニズムを、マーシャリングと呼びます。</span><span class="sxs-lookup"><span data-stu-id="fa188-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="fa188-121">マーシャリングには、スタブオブジェクトとプロキシオブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fa188-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="fa188-122">これらの特別なオブジェクトによって、マーシャリングするオブジェクトのインターフェイスのパラメーターがパッケージ化され、これらのパラメーターが他のスレッドに転送されて、到着時にアンパッケージ化されます。</span><span class="sxs-lookup"><span data-stu-id="fa188-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="fa188-123">2つのマルチスレッドモデル間の競合は、OLE "ライトウェイト" リモートプロシージャコールまたは LRPC を使用して、別のプロセスに、フリースレッドの MAPI オブジェクトが送信されるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="fa188-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="fa188-124">LRPC は、オブジェクトとその呼び出し元との間のアパートメントスレッド動作を使用して、オブジェクトのセマンティクスを解放スレッドからアパートメントスレッドに変更します。</span><span class="sxs-lookup"><span data-stu-id="fa188-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="fa188-125">この競合につながる MAPI の状況を認識することは、クライアントとサービスプロバイダーが問題の発生を防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fa188-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="fa188-126">MAPI オブジェクトにアクセスするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="fa188-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="fa188-127">[MAPILogonEx](mapilogonex.md)から返されるセッションオブジェクトなど、クライアントのプロセスにリンクされているサービスプロバイダーまたは MAPI によって返されるインターフェイスポインターを使用して、そのメソッドへの直接呼び出しを実行します。</span><span class="sxs-lookup"><span data-stu-id="fa188-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="fa188-128">任意のサービスプロバイダーから返されるインターフェイスポインター ( [imapifolder:: copyfolder](imapifolder-copyfolder.md)内の別のフォルダーからコピーされた folder オブジェクトなど) を使用して、そのメソッドを間接的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fa188-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="fa188-129">コールバック関数 ( [IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドなど) を使用して、サービスプロバイダーに渡されるか、**アドバイズ**呼び出しの MAPI に渡されるか、または時間のかかる操作の進行状況を示すことができるメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa188-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

