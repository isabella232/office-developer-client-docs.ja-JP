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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 75ef8d6f2134e0269745f92dab1f790228692853
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800615"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="52758-103">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="52758-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="52758-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52758-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52758-105">メッセージを操作して、このような操作に応答するフォーム ビューアー コード (通常はクライアント アプリケーション) によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="52758-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52758-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="52758-106">Header file:</span></span>  <br/> |<span data-ttu-id="52758-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="52758-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="52758-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="52758-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="52758-109">サイト オブジェクトのメッセージ</span><span class="sxs-lookup"><span data-stu-id="52758-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="52758-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="52758-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="52758-111">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="52758-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="52758-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="52758-112">Called by:</span></span>  <br/> |<span data-ttu-id="52758-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="52758-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="52758-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="52758-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="52758-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="52758-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="52758-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="52758-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="52758-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="52758-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="52758-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="52758-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="52758-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="52758-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="52758-120">現在のメッセージを作成または開いたの MAPI セッションを返します。</span><span class="sxs-lookup"><span data-stu-id="52758-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="52758-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="52758-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="52758-122">このようなストアが存在する場合は、現在のメッセージを含むメッセージ ストアを返します。</span><span class="sxs-lookup"><span data-stu-id="52758-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="52758-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="52758-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="52758-124">このようなフォルダーが存在する場合は、フォルダーを現在のメッセージを作成または開いたを返します。</span><span class="sxs-lookup"><span data-stu-id="52758-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="52758-125">自動インクリメント</span><span class="sxs-lookup"><span data-stu-id="52758-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="52758-126">現在のメッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="52758-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="52758-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="52758-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="52758-128">フォーム サーバーが別のフォームのサーバーを開くに使用できるフォーム マネージャーのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="52758-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="52758-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="52758-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="52758-130">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="52758-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="52758-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="52758-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="52758-132">現在のメッセージをフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="52758-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="52758-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="52758-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="52758-134">現在のメッセージをフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="52758-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="52758-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="52758-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="52758-136">現在のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="52758-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="52758-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="52758-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="52758-138">現在のメッセージを保存するように要求します。</span><span class="sxs-lookup"><span data-stu-id="52758-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="52758-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="52758-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="52758-140">現在のメッセージが配信のキューに置かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="52758-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="52758-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="52758-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="52758-142">メッセージに関するメッセージのサイト オブジェクトの現在のメッセージのサイトの機能に対応する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="52758-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="52758-143">発生しました</span><span class="sxs-lookup"><span data-stu-id="52758-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="52758-144">メッセージ サイト オブジェクトに発生する前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="52758-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52758-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="52758-145">See also</span></span>



[<span data-ttu-id="52758-146">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="52758-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

