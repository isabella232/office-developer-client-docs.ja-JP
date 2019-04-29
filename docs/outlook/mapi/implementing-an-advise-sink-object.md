---
title: アドバイズシンクオブジェクトの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ecaad65d28f74b843b86ca82dab9a833ade77363
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412108"
---
# <a name="implementing-an-advise-sink-object"></a><span data-ttu-id="04520-103">アドバイズシンクオブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="04520-103">Implementing an Advise Sink Object</span></span>

  
  
<span data-ttu-id="04520-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04520-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04520-105">クライアントは、独自のアドバイズシンクオブジェクトを実装するか、ユーティリティ関数[HrAllocAdviseSink](hrallocadvisesink.md)を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="04520-105">A client can either implement its own advise sink objects or use a utility function, [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="04520-106">**HrAllocAdviseSink**は、コールバック関数を呼び出す**onnotify**の実装を使用して、アドバイズシンクオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="04520-106">**HrAllocAdviseSink** creates an advise sink object with an implementation of **OnNotify** that invokes a callback function.</span></span> 
  
<span data-ttu-id="04520-107">**HrAllocAdviseSink**を使用することには、長所と短所があります。</span><span class="sxs-lookup"><span data-stu-id="04520-107">There are advantages and disadvantages to using **HrAllocAdviseSink**.</span></span> <span data-ttu-id="04520-108">作業を節約することはできますが、作成するアドバイズシンクオブジェクトをカウントする参照を制御することはできません。</span><span class="sxs-lookup"><span data-stu-id="04520-108">It can save work, but it provides no control over reference counting the advise sink object that it creates.</span></span> <span data-ttu-id="04520-109">そのため、アドバイズシンクのリリースを慎重に制御する必要があるクライアント、またはアドバイズシンクの間に相互依存関係があり、別のクライアントオブジェクトが独自の**IMAPIAdviseSink**実装を構築して使用**しないようにする必要があります。HrAllocAdviseSink**全体。</span><span class="sxs-lookup"><span data-stu-id="04520-109">Therefore, clients that need to carefully control their advise sink's release or that have interdependencies between their advise sink and another client object should construct their own **IMAPIAdviseSink** implementation and avoid using **HrAllocAdviseSink** altogether.</span></span> 
  
<span data-ttu-id="04520-110">独自のアドバイズシンクを実装するクライアントは、他のオブジェクトに関連していないか、または他のオブジェクトに依存していない独立したオブジェクトにすることにより、参照カウントおよびオブジェクトのリリースに発生する可能性のある問題を排除します。</span><span class="sxs-lookup"><span data-stu-id="04520-110">A client implementing its own advise sink should make it an independent object not related to or dependent upon any other objects so as to eliminate potential complications in reference counting and object release.</span></span> <span data-ttu-id="04520-111">ただし、別のオブジェクトの一部としてアドバイズシンクを実装する必要がある場合、またはデータメンバーとして別のオブジェクトへの後方ポインターが含まれている場合は、2つの個別の参照カウントを保持することをお勧めします。1つは、アドバイズシンクによって参照されるオブジェクト用、もう1つアドバイズシンク。</span><span class="sxs-lookup"><span data-stu-id="04520-111">However, if you must implement your advise sink as part of another object or include a back pointer to another object as a data member, it is recommended that two separate reference counts be maintained: one for the object referenced by the advise sink and one for the advise sink.</span></span> 
  
<span data-ttu-id="04520-112">参照されるオブジェクトの参照カウントがゼロになると、そのすべてのメソッドが失敗し、その vtable が破棄される可能性がありますが、アドバイズシンクのメモリは、その参照カウントがゼロになるまで、そのまま維持されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="04520-112">When the reference count of the referenced object falls to zero, all of its methods can fail and its vtable can be destroyed, but the memory for the advise sink must remain intact until after its reference count also falls to zero.</span></span> <span data-ttu-id="04520-113">これは、アドバイズシンクの**Release**メソッドが、参照カウントをデクリメントして、そのカウントが0に達したときにオブジェクトの破棄を完了する必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="04520-113">This means that the advise sink's **Release** method must decrement its reference count and finish destroying the object when that count reaches zero.</span></span> <span data-ttu-id="04520-114">2つの異なる参照カウントが保持されていない場合、そのアドバイズシンクは、そのオブジェクトの**解放**プロセスの一部として誤って破棄するのが簡単です。</span><span class="sxs-lookup"><span data-stu-id="04520-114">If two separate reference counts are not maintained, it would be easy to inadvertently destroy the advise sink as part of the encompassing object's **Release** process.</span></span> 
  
<span data-ttu-id="04520-115">**HrAllocAdviseSink**を使用してアドバイズシンクを実装するクライアントは、別のアドバイズシンクオブジェクトのメソッドとしてコールバック関数を含めないように注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04520-115">Clients using **HrAllocAdviseSink** to implement an advise sink must be equally careful not to include their callback function as a method in another advise sink object.</span></span> <span data-ttu-id="04520-116">C++ クライアントでは、これを実行して、_この_ポインターをパラメーターとして渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="04520-116">For C++ clients, it is tempting to do this and pass the  _this_ pointer as a parameter.</span></span> <span data-ttu-id="04520-117">クライアントは通常、参照カウントが0に達したときにオブジェクトを解放するため、これは危険な戦略です。</span><span class="sxs-lookup"><span data-stu-id="04520-117">This is a dangerous strategy because clients typically free an object when its reference count reaches zero.</span></span> <span data-ttu-id="04520-118">アドバイズシンクオブジェクトのメモリを解放すると、_この_ポインターが無効であると表示されます。</span><span class="sxs-lookup"><span data-stu-id="04520-118">Freeing the memory for the advise sink object would render the  _this_ pointer invalid.</span></span> 
  
<span data-ttu-id="04520-119">イベントの種類とアドバイズソースに応じて、 **onnotify**メソッドはさまざまな方法でイベントを処理できます。</span><span class="sxs-lookup"><span data-stu-id="04520-119">Depending on the type of event and the advise source, your **OnNotify** method can handle events in various ways.</span></span> <span data-ttu-id="04520-120">次の表に、いくつかの標準イベントを処理する方法に関する提案を示します。</span><span class="sxs-lookup"><span data-stu-id="04520-120">The following table offers suggestions in how to handle some of the standard events.</span></span> 
  
|<span data-ttu-id="04520-121">**イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="04520-121">**Type of event**</span></span>|<span data-ttu-id="04520-122">**onnotify での処理**</span><span class="sxs-lookup"><span data-stu-id="04520-122">**Handling in OnNotify**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04520-123">移動されたオブジェクト</span><span class="sxs-lookup"><span data-stu-id="04520-123">Object moved</span></span>  <br/> |<span data-ttu-id="04520-124">移動したオブジェクトの元の親が新しい親に関連付けられている場合は、階層の最上位のフォルダーまたはアドレス帳コンテナーから始まるビューを更新します。</span><span class="sxs-lookup"><span data-stu-id="04520-124">If the moved object's original parent is related to the new parent, update the view beginning with the folder or address book container highest in the hierarchy.</span></span> <span data-ttu-id="04520-125">2つの親コンテナーが関連付けられていない場合は、両方のビューを更新します。</span><span class="sxs-lookup"><span data-stu-id="04520-125">If the two parent containers are unrelated, update both of their views.</span></span>  <br/> |
|<span data-ttu-id="04520-126">新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="04520-126">New message</span></span>  <br/> |<span data-ttu-id="04520-127">ユーザーインターフェイスを変更して、1つまたは複数の新しいメッセージが到着したことをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="04520-127">Change the user interface to inform the user of the arrival of one or more new messages.</span></span> <span data-ttu-id="04520-128">受信フォルダーを現在のビューに配置します。</span><span class="sxs-lookup"><span data-stu-id="04520-128">Place the receive folder in the current view.</span></span>  <br/> |
|<span data-ttu-id="04520-129">Error</span><span class="sxs-lookup"><span data-stu-id="04520-129">Error</span></span>  <br/> |<span data-ttu-id="04520-130">セッション以外のすべてのオブジェクトについて、必要に応じてエラーをログに記録し、を返します。</span><span class="sxs-lookup"><span data-stu-id="04520-130">For all objects except the session, log the error if necessary and return.</span></span> <span data-ttu-id="04520-131">session オブジェクトの場合は、可能であればログオフします。</span><span class="sxs-lookup"><span data-stu-id="04520-131">For the session object, log off if possible.</span></span>  <br/> |
|<span data-ttu-id="04520-132">検索の完了</span><span class="sxs-lookup"><span data-stu-id="04520-132">Search complete</span></span>  <br/> |<span data-ttu-id="04520-133">処理は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="04520-133">No processing necessary.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="04520-134">通知ハンドラーは再入可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="04520-134">Notification handlers should be reentrant.</span></span> 
  

