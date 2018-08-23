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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cffa3024b8533f07f8f76fa5bbac219e23d61bdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589505"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="a634b-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a634b-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="a634b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a634b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a634b-105">メッセージを操作して、このような操作に応答するフォーム ビューアー コード (通常はクライアント アプリケーション) によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a634b-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a634b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a634b-106">Header file:</span></span>  <br/> |<span data-ttu-id="a634b-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a634b-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a634b-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="a634b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a634b-109">サイト オブジェクトのメッセージ</span><span class="sxs-lookup"><span data-stu-id="a634b-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="a634b-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a634b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a634b-111">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="a634b-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="a634b-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a634b-112">Called by:</span></span>  <br/> |<span data-ttu-id="a634b-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="a634b-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="a634b-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="a634b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a634b-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="a634b-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="a634b-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="a634b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a634b-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="a634b-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a634b-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="a634b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a634b-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="a634b-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="a634b-120">現在のメッセージを作成または開いたの MAPI セッションを返します。</span><span class="sxs-lookup"><span data-stu-id="a634b-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="a634b-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="a634b-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="a634b-122">このようなストアが存在する場合は、現在のメッセージを含むメッセージ ストアを返します。</span><span class="sxs-lookup"><span data-stu-id="a634b-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="a634b-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="a634b-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="a634b-124">このようなフォルダーが存在する場合は、フォルダーを現在のメッセージを作成または開いたを返します。</span><span class="sxs-lookup"><span data-stu-id="a634b-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="a634b-125">自動インクリメント</span><span class="sxs-lookup"><span data-stu-id="a634b-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="a634b-126">現在のメッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="a634b-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="a634b-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="a634b-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="a634b-128">フォーム サーバーが別のフォームのサーバーを開くに使用できるフォーム マネージャーのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="a634b-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="a634b-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="a634b-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="a634b-130">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="a634b-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="a634b-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="a634b-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="a634b-132">現在のメッセージをフォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a634b-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="a634b-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="a634b-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="a634b-134">現在のメッセージをフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="a634b-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="a634b-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="a634b-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="a634b-136">現在のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="a634b-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="a634b-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="a634b-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="a634b-138">現在のメッセージを保存するように要求します。</span><span class="sxs-lookup"><span data-stu-id="a634b-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="a634b-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="a634b-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="a634b-140">現在のメッセージが配信のキューに置かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="a634b-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="a634b-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="a634b-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="a634b-142">メッセージに関するメッセージのサイト オブジェクトの現在のメッセージのサイトの機能に対応する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="a634b-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="a634b-143">発生しました</span><span class="sxs-lookup"><span data-stu-id="a634b-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="a634b-144">メッセージ サイト オブジェクトに発生する前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="a634b-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a634b-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="a634b-145">See also</span></span>



[<span data-ttu-id="a634b-146">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a634b-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

