---
title: アドバイス シンク オブジェクトの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a95222f8ec75c519558636cf54111f28cbe14066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800928"
---
# <a name="implementing-an-advise-sink-object"></a><span data-ttu-id="b6557-103">アドバイス シンク オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="b6557-103">Implementing an Advise Sink Object</span></span>

  
  
<span data-ttu-id="b6557-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6557-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6557-105">クライアント独自のアドバイズ シンク オブジェクトを実装するか、 [HrAllocAdviseSink](hrallocadvisesink.md)のユーティリティ関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="b6557-105">A client can either implement its own advise sink objects or use a utility function, [HrAllocAdviseSink](hrallocadvisesink.md).</span></span> <span data-ttu-id="b6557-106">**HrAllocAdviseSink**は、コールバック関数を呼び出す**OnNotify**の実装とアドバイズ シンク オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b6557-106">**HrAllocAdviseSink** creates an advise sink object with an implementation of **OnNotify** that invokes a callback function.</span></span> 
  
<span data-ttu-id="b6557-107">**HrAllocAdviseSink**を使用してに長所と短所があります。</span><span class="sxs-lookup"><span data-stu-id="b6557-107">There are advantages and disadvantages to using **HrAllocAdviseSink**.</span></span> <span data-ttu-id="b6557-108">作業を保存することができますが、参照カウントのアドバイズ シンク オブジェクトを作成する上でのコントロールが用意されていません。</span><span class="sxs-lookup"><span data-stu-id="b6557-108">It can save work, but it provides no control over reference counting the advise sink object that it creates.</span></span> <span data-ttu-id="b6557-109">したがって、クライアントがアドバイズ シンクのリリースを慎重に制御する必要があるか、アドバイズ シンクと別のクライアント オブジェクトとの間の相互依存関係があるが**IMAPIAdviseSink**の独自の実装を構築し、**を使用しないようにする必要があります。HrAllocAdviseSink**完全です。</span><span class="sxs-lookup"><span data-stu-id="b6557-109">Therefore, clients that need to carefully control their advise sink's release or that have interdependencies between their advise sink and another client object should construct their own **IMAPIAdviseSink** implementation and avoid using **HrAllocAdviseSink** altogether.</span></span> 
  
<span data-ttu-id="b6557-110">クライアント独自のアドバイズ シンクを実装する必要がありますように独立したオブジェクトに関連するまたはその他のオブジェクトの参照カウントと、オブジェクトのリリースでの潜在的な複雑な問題をなくすために依存しません。</span><span class="sxs-lookup"><span data-stu-id="b6557-110">A client implementing its own advise sink should make it an independent object not related to or dependent upon any other objects so as to eliminate potential complications in reference counting and object release.</span></span> <span data-ttu-id="b6557-111">ただし場合は、別のオブジェクトの一部として、アドバイズ シンクを実装する必要がありますかデータ メンバーとして別のオブジェクトへのバック ポインターを含めると、お勧め 2 つの個別の参照カウントを維持する: アドバイズ シンクとのいずれかによって参照されるオブジェクトのいずれか、シンクをアドバイスします。</span><span class="sxs-lookup"><span data-stu-id="b6557-111">However, if you must implement your advise sink as part of another object or include a back pointer to another object as a data member, it is recommended that two separate reference counts be maintained: one for the object referenced by the advise sink and one for the advise sink.</span></span> 
  
<span data-ttu-id="b6557-112">参照されるオブジェクトの参照カウントがゼロに達する、そのメソッドのすべてが失敗することができますとその vtable を破棄することができます、ですがアドバイズ シンク用のメモリ必要がありますまままで、参照カウントがゼロになるも後です。</span><span class="sxs-lookup"><span data-stu-id="b6557-112">When the reference count of the referenced object falls to zero, all of its methods can fail and its vtable can be destroyed, but the memory for the advise sink must remain intact until after its reference count also falls to zero.</span></span> <span data-ttu-id="b6557-113">つまり、アドバイズ シンクの**Release**メソッドが、参照カウントをデクリメントして完了、その数が 0 になったときに、オブジェクトを破棄する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6557-113">This means that the advise sink's **Release** method must decrement its reference count and finish destroying the object when that count reaches zero.</span></span> <span data-ttu-id="b6557-114">2 つの個別の参照カウントは変更されない、外側にあるオブジェクトの**リリース**プロセスの一環としてアドバイズ シンクを誤って破棄するのには簡単になります。</span><span class="sxs-lookup"><span data-stu-id="b6557-114">If two separate reference counts are not maintained, it would be easy to inadvertently destroy the advise sink as part of the encompassing object's **Release** process.</span></span> 
  
<span data-ttu-id="b6557-115">アドバイズ シンクを実装するために**HrAllocAdviseSink**を使用するクライアントは、アドバイズ シンク オブジェクトを別の方法として、コールバック関数を含める必要はありません同じように注意が必要である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6557-115">Clients using **HrAllocAdviseSink** to implement an advise sink must be equally careful not to include their callback function as a method in another advise sink object.</span></span> <span data-ttu-id="b6557-116">C++ クライアントの場合は、することは避けてこの操作を行うし、_この_ポインターをパラメーターとして渡します。</span><span class="sxs-lookup"><span data-stu-id="b6557-116">For C++ clients, it is tempting to do this and pass the  _this_ pointer as a parameter.</span></span> <span data-ttu-id="b6557-117">これは、クライアントは、その参照カウントがゼロになると、通常オブジェクトを解放するために危険な戦略です。</span><span class="sxs-lookup"><span data-stu-id="b6557-117">This is a dangerous strategy because clients typically free an object when its reference count reaches zero.</span></span> <span data-ttu-id="b6557-118">アドバイズ シンク オブジェクトのメモリの解放が無効になる_この_ポインター。</span><span class="sxs-lookup"><span data-stu-id="b6557-118">Freeing the memory for the advise sink object would render the  _this_ pointer invalid.</span></span> 
  
<span data-ttu-id="b6557-119">**OnNotify**メソッドは、イベントやアドバイスのソースの種類に応じて、さまざまな方法でのイベントを処理できます。</span><span class="sxs-lookup"><span data-stu-id="b6557-119">Depending on the type of event and the advise source, your **OnNotify** method can handle events in various ways.</span></span> <span data-ttu-id="b6557-120">次の表は、標準のイベントを処理する方法のご提案を提供します。</span><span class="sxs-lookup"><span data-stu-id="b6557-120">The following table offers suggestions in how to handle some of the standard events.</span></span> 
  
|<span data-ttu-id="b6557-121">**イベントの種類**</span><span class="sxs-lookup"><span data-stu-id="b6557-121">**Type of event**</span></span>|<span data-ttu-id="b6557-122">**OnNotify での処理**</span><span class="sxs-lookup"><span data-stu-id="b6557-122">**Handling in OnNotify**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6557-123">オブジェクトの移動</span><span class="sxs-lookup"><span data-stu-id="b6557-123">Object moved</span></span>  <br/> |<span data-ttu-id="b6557-124">移動したオブジェクトの元の親が新しい親に関連付けられている場合は、フォルダーまたはアドレス帳の階層の最上位のコンテナーでビューの先頭を更新します。</span><span class="sxs-lookup"><span data-stu-id="b6557-124">If the moved object's original parent is related to the new parent, update the view beginning with the folder or address book container highest in the hierarchy.</span></span> <span data-ttu-id="b6557-125">2 つの親コンテナーが関連する場合は、そのビューの両方を更新します。</span><span class="sxs-lookup"><span data-stu-id="b6557-125">If the two parent containers are unrelated, update both of their views.</span></span>  <br/> |
|<span data-ttu-id="b6557-126">新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="b6557-126">New message</span></span>  <br/> |<span data-ttu-id="b6557-127">1 つまたは複数の新しいメッセージの到着をユーザーに通知するユーザー インターフェイスを変更します。</span><span class="sxs-lookup"><span data-stu-id="b6557-127">Change the user interface to inform the user of the arrival of one or more new messages.</span></span> <span data-ttu-id="b6557-128">受信フォルダーを現在のビューに配置します。</span><span class="sxs-lookup"><span data-stu-id="b6557-128">Place the receive folder in the current view.</span></span>  <br/> |
|<span data-ttu-id="b6557-129">エラー</span><span class="sxs-lookup"><span data-stu-id="b6557-129">Error</span></span>  <br/> |<span data-ttu-id="b6557-130">セッションを除くすべてのオブジェクト、必要であれば戻り値エラーをログに記録します。</span><span class="sxs-lookup"><span data-stu-id="b6557-130">For all objects except the session, log the error if necessary and return.</span></span> <span data-ttu-id="b6557-131">セッション オブジェクトでは、ログオフ可能な場合です。</span><span class="sxs-lookup"><span data-stu-id="b6557-131">For the session object, log off if possible.</span></span>  <br/> |
|<span data-ttu-id="b6557-132">検索が完了しました</span><span class="sxs-lookup"><span data-stu-id="b6557-132">Search complete</span></span>  <br/> |<span data-ttu-id="b6557-133">処理は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="b6557-133">No processing necessary.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b6557-134">通知ハンドラーは再入可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b6557-134">Notification handlers should be reentrant.</span></span> 
  

