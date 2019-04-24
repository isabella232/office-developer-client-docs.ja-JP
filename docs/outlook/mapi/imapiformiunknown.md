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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321778"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="a697d-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a697d-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="a697d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a697d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a697d-105">フォームビューアーがフォームビューのコンテキストとフォームの通知を操作したり、フォームの動詞を実行したり、フォームをシャットダウンしたりできるようにします。</span><span class="sxs-lookup"><span data-stu-id="a697d-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a697d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a697d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a697d-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="a697d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a697d-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="a697d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a697d-109">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a697d-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="a697d-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="a697d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a697d-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="a697d-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="a697d-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a697d-112">Called by:</span></span>  <br/> |<span data-ttu-id="a697d-113">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="a697d-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="a697d-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="a697d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a697d-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="a697d-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="a697d-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="a697d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a697d-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="a697d-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a697d-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="a697d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a697d-119">setviewcontext</span><span class="sxs-lookup"><span data-stu-id="a697d-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="a697d-120">フォームのビューコンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="a697d-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="a697d-121">getviewcontext</span><span class="sxs-lookup"><span data-stu-id="a697d-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="a697d-122">フォームの現在のビューコンテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="a697d-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="a697d-123">shutdownform</span><span class="sxs-lookup"><span data-stu-id="a697d-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="a697d-124">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a697d-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="a697d-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="a697d-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="a697d-126">フォームが特定の動詞に関連付けられている任意のタスクを実行するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="a697d-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="a697d-127">助言</span><span class="sxs-lookup"><span data-stu-id="a697d-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="a697d-128">フォームに影響を与えるイベントに関する通知に対してフォームビューアーを登録します。</span><span class="sxs-lookup"><span data-stu-id="a697d-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="a697d-129">アドバイズ</span><span class="sxs-lookup"><span data-stu-id="a697d-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="a697d-130">以前に呼び出し先の**アドバイズ**によって設定されたフォームビューアーでの通知の登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="a697d-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="a697d-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a697d-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="a697d-132">form オブジェクトの前に発生したエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="a697d-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a697d-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a697d-133">See also</span></span>



[<span data-ttu-id="a697d-134">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="a697d-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

