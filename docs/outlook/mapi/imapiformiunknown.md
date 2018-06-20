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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fce8bc45d5cc87c238288653ab989b62076ad451
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800553"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="029e7-103">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="029e7-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="029e7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="029e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="029e7-105">フォームの閲覧者は、フォーム ビューのコンテキストと、フォームの動詞を実行して、フォームをシャット ダウンするのにはフォームの通知を有効にします。</span><span class="sxs-lookup"><span data-stu-id="029e7-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="029e7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="029e7-106">Header file:</span></span>  <br/> |<span data-ttu-id="029e7-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="029e7-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="029e7-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="029e7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="029e7-109">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="029e7-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="029e7-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="029e7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="029e7-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="029e7-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="029e7-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="029e7-112">Called by:</span></span>  <br/> |<span data-ttu-id="029e7-113">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="029e7-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="029e7-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="029e7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="029e7-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="029e7-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="029e7-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="029e7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="029e7-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="029e7-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="029e7-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="029e7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="029e7-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="029e7-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="029e7-120">フォームのビュー コンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="029e7-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="029e7-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="029e7-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="029e7-122">フォームの現在のビュー コンテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="029e7-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="029e7-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="029e7-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="029e7-124">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="029e7-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="029e7-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="029e7-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="029e7-126">フォームは、タスクをどのような実行要求は、特定の動作に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="029e7-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="029e7-127">アドバイス</span><span class="sxs-lookup"><span data-stu-id="029e7-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="029e7-128">フォーム ビューアーの形式に影響するイベント通知を登録します。</span><span class="sxs-lookup"><span data-stu-id="029e7-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="029e7-129">アドバイズ中止します。</span><span class="sxs-lookup"><span data-stu-id="029e7-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="029e7-130">**アドバイズ**を呼び出すことによって確立されていたフォーム ビューアーを使用して通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="029e7-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="029e7-131">発生しました</span><span class="sxs-lookup"><span data-stu-id="029e7-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="029e7-132">前の form オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="029e7-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="029e7-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="029e7-133">See also</span></span>



[<span data-ttu-id="029e7-134">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="029e7-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

