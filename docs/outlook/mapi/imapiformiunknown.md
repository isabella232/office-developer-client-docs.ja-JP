---
title: imapiform IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436385"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="bd8ac-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd8ac-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="bd8ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd8ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd8ac-105">フォームビューアーがフォームビューのコンテキストとフォームの通知を操作したり、フォームの動詞を実行したり、フォームをシャットダウンしたりできるようにします。</span><span class="sxs-lookup"><span data-stu-id="bd8ac-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd8ac-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bd8ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd8ac-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="bd8ac-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="bd8ac-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="bd8ac-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="bd8ac-109">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="bd8ac-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="bd8ac-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="bd8ac-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="bd8ac-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="bd8ac-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="bd8ac-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="bd8ac-112">Called by:</span></span>  <br/> |<span data-ttu-id="bd8ac-113">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="bd8ac-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="bd8ac-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="bd8ac-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bd8ac-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="bd8ac-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="bd8ac-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="bd8ac-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="bd8ac-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="bd8ac-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bd8ac-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="bd8ac-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="bd8ac-119">setviewcontext</span><span class="sxs-lookup"><span data-stu-id="bd8ac-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="bd8ac-120">フォームのビューコンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="bd8ac-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="bd8ac-121">getviewcontext</span><span class="sxs-lookup"><span data-stu-id="bd8ac-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="bd8ac-122">フォームの現在のビューコンテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="bd8ac-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="bd8ac-123">shutdownform</span><span class="sxs-lookup"><span data-stu-id="bd8ac-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="bd8ac-124">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bd8ac-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="bd8ac-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="bd8ac-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="bd8ac-126">フォームが特定の動詞に関連付けられている任意のタスクを実行するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="bd8ac-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="bd8ac-127">助言</span><span class="sxs-lookup"><span data-stu-id="bd8ac-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="bd8ac-128">フォームに影響を与えるイベントに関する通知に対してフォームビューアーを登録します。</span><span class="sxs-lookup"><span data-stu-id="bd8ac-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="bd8ac-129">アドバイズ</span><span class="sxs-lookup"><span data-stu-id="bd8ac-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="bd8ac-130">以前に呼び出し先の**アドバイズ**によって設定されたフォームビューアーでの通知の登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="bd8ac-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="bd8ac-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="bd8ac-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="bd8ac-132">form オブジェクトの前に発生したエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="bd8ac-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd8ac-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd8ac-133">See also</span></span>



[<span data-ttu-id="bd8ac-134">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="bd8ac-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

