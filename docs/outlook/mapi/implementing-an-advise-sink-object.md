---
title: Advise Sink オブジェクトの実装
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
# <a name="implementing-an-advise-sink-object"></a><span data-ttu-id="25bbb-103">Advise Sink オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="25bbb-103">Implementing an Advise Sink Object</span></span>

  
  
<span data-ttu-id="25bbb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25bbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25bbb-105">クライアントは、独自のアアドバイス シンク オブジェクトを実装するか、ユーティリティ関数 [HrAllocAdviseSink を使用できます](hrallocadvisesink.md)。</span><span class="sxs-lookup"><span data-stu-id="25bbb-105">A client can either implement its own advise sink objects or use a utility function, [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="25bbb-106">**HrAllocAdviseSink** は、コールバック関数を呼び出す **OnNotify** の実装を持つアアドバイス シンク オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="25bbb-106">**HrAllocAdviseSink** creates an advise sink object with an implementation of **OnNotify** that invokes a callback function.</span></span> 
  
<span data-ttu-id="25bbb-107">**HrAllocAdviseSink** を使用する利点と欠点があります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-107">There are advantages and disadvantages to using **HrAllocAdviseSink**.</span></span> <span data-ttu-id="25bbb-108">作業を保存できますが、作成するアアドバイス シンク オブジェクトをカウントする参照を制御しません。</span><span class="sxs-lookup"><span data-stu-id="25bbb-108">It can save work, but it provides no control over reference counting the advise sink object that it creates.</span></span> <span data-ttu-id="25bbb-109">したがって、アドバイス シンクのリリースを慎重に制御する必要があるクライアント、またはアアドバイス シンクと別のクライアント オブジェクトの間に相互依存関係があるクライアントは、独自の **IMAPIAdviseSink** 実装を構築し **、HrAllocAdviseSink** の使用を完全に回避する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-109">Therefore, clients that need to carefully control their advise sink's release or that have interdependencies between their advise sink and another client object should construct their own **IMAPIAdviseSink** implementation and avoid using **HrAllocAdviseSink** altogether.</span></span> 
  
<span data-ttu-id="25bbb-110">独自のアアドバイス シンクを実装するクライアントは、参照カウントとオブジェクトの解放における潜在的な複雑性を排除するために、他のオブジェクトに関連しない、または依存しない独立したオブジェクトにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-110">A client implementing its own advise sink should make it an independent object not related to or dependent upon any other objects so as to eliminate potential complications in reference counting and object release.</span></span> <span data-ttu-id="25bbb-111">ただし、別のオブジェクトの一部としてアアドバイス シンクを実装する必要がある場合や、別のオブジェクトへの戻りポインターをデータ メンバーとして含める必要がある場合は、2 つの個別の参照カウント (1 つは、アアドバイス シンクで参照されるオブジェクト用とアアドバイス シンク用) を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-111">However, if you must implement your advise sink as part of another object or include a back pointer to another object as a data member, it is recommended that two separate reference counts be maintained: one for the object referenced by the advise sink and one for the advise sink.</span></span> 
  
<span data-ttu-id="25bbb-112">参照先のオブジェクトの参照カウントが 0 に設定されると、すべてのメソッドが失敗し、その vtable を破棄できますが、参照カウントが 0 に落ちるまで、アアドバイス シンクのメモリはそのまま残る必要があります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-112">When the reference count of the referenced object falls to zero, all of its methods can fail and its vtable can be destroyed, but the memory for the advise sink must remain intact until after its reference count also falls to zero.</span></span> <span data-ttu-id="25bbb-113">つまり、アアドバイス シンクの **Release** メソッドは、参照カウントをデクレメントし、そのカウントが 0 に達したときにオブジェクトの破棄を終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-113">This means that the advise sink's **Release** method must decrement its reference count and finish destroying the object when that count reaches zero.</span></span> <span data-ttu-id="25bbb-114">2 つの個別の参照カウントを維持しない場合、対象オブジェクトの Release プロセスの一部として、アアドバイス シンクを誤って破棄するのは **簡単** です。</span><span class="sxs-lookup"><span data-stu-id="25bbb-114">If two separate reference counts are not maintained, it would be easy to inadvertently destroy the advise sink as part of the encompassing object's **Release** process.</span></span> 
  
<span data-ttu-id="25bbb-115">**HrAllocAdviseSink** を使用してアアドバイス シンクを実装するクライアントは、コールバック関数を別のアアドバイス シンク オブジェクトにメソッドとして含めないように同様に注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-115">Clients using **HrAllocAdviseSink** to implement an advise sink must be equally careful not to include their callback function as a method in another advise sink object.</span></span> <span data-ttu-id="25bbb-116">C++ クライアントの場合、これを行い、この  _ポインターをパラメーター_ として渡すのは魅力的です。</span><span class="sxs-lookup"><span data-stu-id="25bbb-116">For C++ clients, it is tempting to do this and pass the  _this_ pointer as a parameter.</span></span> <span data-ttu-id="25bbb-117">クライアントは通常、参照カウントが 0 に達したときにオブジェクトを解放する場合、これは危険な戦略です。</span><span class="sxs-lookup"><span data-stu-id="25bbb-117">This is a dangerous strategy because clients typically free an object when its reference count reaches zero.</span></span> <span data-ttu-id="25bbb-118">アアドバイス シンク オブジェクトのメモリを解放すると、このポインターは  _無効_ になります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-118">Freeing the memory for the advise sink object would render the  _this_ pointer invalid.</span></span> 
  
<span data-ttu-id="25bbb-119">イベントの種類とアドバイス ソースに応じて **、OnNotify** メソッドはさまざまな方法でイベントを処理できます。</span><span class="sxs-lookup"><span data-stu-id="25bbb-119">Depending on the type of event and the advise source, your **OnNotify** method can handle events in various ways.</span></span> <span data-ttu-id="25bbb-120">次の表では、標準的なイベントの一部を処理する方法について提案します。</span><span class="sxs-lookup"><span data-stu-id="25bbb-120">The following table offers suggestions in how to handle some of the standard events.</span></span> 
  
|<span data-ttu-id="25bbb-121">**イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="25bbb-121">**Type of event**</span></span>|<span data-ttu-id="25bbb-122">**OnNotify での処理**</span><span class="sxs-lookup"><span data-stu-id="25bbb-122">**Handling in OnNotify**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25bbb-123">オブジェクトの移動</span><span class="sxs-lookup"><span data-stu-id="25bbb-123">Object moved</span></span>  <br/> |<span data-ttu-id="25bbb-124">移動したオブジェクトの元の親が新しい親に関連付けされている場合は、階層内で最も高いフォルダーまたはアドレス帳コンテナーで始まるビューを更新します。</span><span class="sxs-lookup"><span data-stu-id="25bbb-124">If the moved object's original parent is related to the new parent, update the view beginning with the folder or address book container highest in the hierarchy.</span></span> <span data-ttu-id="25bbb-125">2 つの親コンテナーが関連付けされていない場合は、両方のビューを更新します。</span><span class="sxs-lookup"><span data-stu-id="25bbb-125">If the two parent containers are unrelated, update both of their views.</span></span>  <br/> |
|<span data-ttu-id="25bbb-126">新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="25bbb-126">New message</span></span>  <br/> |<span data-ttu-id="25bbb-127">ユーザー インターフェイスを変更して、1 つ以上の新しいメッセージの到着をユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="25bbb-127">Change the user interface to inform the user of the arrival of one or more new messages.</span></span> <span data-ttu-id="25bbb-128">現在のビューに受信フォルダーを配置します。</span><span class="sxs-lookup"><span data-stu-id="25bbb-128">Place the receive folder in the current view.</span></span>  <br/> |
|<span data-ttu-id="25bbb-129">Error</span><span class="sxs-lookup"><span data-stu-id="25bbb-129">Error</span></span>  <br/> |<span data-ttu-id="25bbb-130">セッションを除くすべてのオブジェクトに対して、必要に応じてエラーをログに記録し、戻します。</span><span class="sxs-lookup"><span data-stu-id="25bbb-130">For all objects except the session, log the error if necessary and return.</span></span> <span data-ttu-id="25bbb-131">セッション オブジェクトの場合は、可能であればログオフします。</span><span class="sxs-lookup"><span data-stu-id="25bbb-131">For the session object, log off if possible.</span></span>  <br/> |
|<span data-ttu-id="25bbb-132">検索の完了</span><span class="sxs-lookup"><span data-stu-id="25bbb-132">Search complete</span></span>  <br/> |<span data-ttu-id="25bbb-133">処理は不要です。</span><span class="sxs-lookup"><span data-stu-id="25bbb-133">No processing necessary.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="25bbb-134">通知ハンドラーは再入可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="25bbb-134">Notification handlers should be reentrant.</span></span> 
  

