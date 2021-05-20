---
title: IMAPIForm IUnknown
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
# <a name="imapiform--iunknown"></a><span data-ttu-id="747c0-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="747c0-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="747c0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="747c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="747c0-105">フォーム ビューアーがフォーム ビューのコンテキストとフォーム通知を操作したり、フォーム動詞を実行したり、フォームをシャットダウンしたりできます。</span><span class="sxs-lookup"><span data-stu-id="747c0-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="747c0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="747c0-106">Header file:</span></span>  <br/> |<span data-ttu-id="747c0-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="747c0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="747c0-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="747c0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="747c0-109">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="747c0-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="747c0-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="747c0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="747c0-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="747c0-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="747c0-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="747c0-112">Called by:</span></span>  <br/> |<span data-ttu-id="747c0-113">フォーム ビューアー</span><span class="sxs-lookup"><span data-stu-id="747c0-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="747c0-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="747c0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="747c0-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="747c0-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="747c0-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="747c0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="747c0-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="747c0-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="747c0-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="747c0-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="747c0-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="747c0-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="747c0-120">フォームのビュー コンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="747c0-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="747c0-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="747c0-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="747c0-122">フォームの現在のビュー コンテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="747c0-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="747c0-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="747c0-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="747c0-124">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="747c0-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="747c0-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="747c0-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="747c0-126">フォームが特定の動詞に関連付けるタスクを実行する要求。</span><span class="sxs-lookup"><span data-stu-id="747c0-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="747c0-127">アドバイス</span><span class="sxs-lookup"><span data-stu-id="747c0-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="747c0-128">フォームに影響を与えるイベントに関する通知用にフォーム ビューアーを登録します。</span><span class="sxs-lookup"><span data-stu-id="747c0-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="747c0-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="747c0-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="747c0-130">Advise を呼び出して以前に確立されたフォーム ビューアーを使用して通知の登録を **取り消します**。</span><span class="sxs-lookup"><span data-stu-id="747c0-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="747c0-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="747c0-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="747c0-132">フォーム オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="747c0-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="747c0-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="747c0-133">See also</span></span>



[<span data-ttu-id="747c0-134">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="747c0-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

