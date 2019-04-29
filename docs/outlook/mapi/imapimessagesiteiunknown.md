---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433368"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="4843f-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4843f-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="4843f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4843f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4843f-105">メッセージを操作し、そのような操作に応答するフォームビューアコード (通常はクライアントアプリケーション) によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="4843f-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4843f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4843f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4843f-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="4843f-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4843f-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="4843f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4843f-109">メッセージサイトオブジェクト</span><span class="sxs-lookup"><span data-stu-id="4843f-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="4843f-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="4843f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4843f-111">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="4843f-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="4843f-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="4843f-112">Called by:</span></span>  <br/> |<span data-ttu-id="4843f-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4843f-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="4843f-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="4843f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4843f-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="4843f-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="4843f-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="4843f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4843f-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="4843f-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4843f-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="4843f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4843f-119">getsession</span><span class="sxs-lookup"><span data-stu-id="4843f-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="4843f-120">現在のメッセージが作成または開かれた MAPI セッションを返します。</span><span class="sxs-lookup"><span data-stu-id="4843f-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="4843f-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="4843f-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="4843f-122">そのようなストアが存在する場合は、現在のメッセージが含まれているメッセージストアを返します。</span><span class="sxs-lookup"><span data-stu-id="4843f-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="4843f-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="4843f-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="4843f-124">現在のメッセージが作成または開かれたフォルダー (そのフォルダーが存在する場合) を返します。</span><span class="sxs-lookup"><span data-stu-id="4843f-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="4843f-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="4843f-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="4843f-126">現在のメッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="4843f-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="4843f-127">getformmanager</span><span class="sxs-lookup"><span data-stu-id="4843f-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="4843f-128">フォームサーバーが別のフォームサーバーを開くために使用できるフォームマネージャーインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="4843f-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="4843f-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="4843f-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="4843f-130">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="4843f-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="4843f-131">copymessage</span><span class="sxs-lookup"><span data-stu-id="4843f-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="4843f-132">現在のメッセージをフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="4843f-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="4843f-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="4843f-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="4843f-134">現在のメッセージをフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="4843f-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="4843f-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="4843f-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="4843f-136">現在のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="4843f-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="4843f-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="4843f-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="4843f-138">現在のメッセージを保存するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="4843f-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="4843f-139">submitmessage</span><span class="sxs-lookup"><span data-stu-id="4843f-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="4843f-140">現在のメッセージが配信のためにキューに入れられるように要求します。</span><span class="sxs-lookup"><span data-stu-id="4843f-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="4843f-141">getsitestatus</span><span class="sxs-lookup"><span data-stu-id="4843f-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="4843f-142">現在のメッセージのメッセージサイトの機能に関する情報をメッセージサイトオブジェクトから返します。</span><span class="sxs-lookup"><span data-stu-id="4843f-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="4843f-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="4843f-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="4843f-144">メッセージサイトオブジェクトに発生する前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="4843f-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4843f-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="4843f-145">See also</span></span>



[<span data-ttu-id="4843f-146">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="4843f-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

