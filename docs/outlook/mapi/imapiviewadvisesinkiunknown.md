---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800860"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="e5152-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5152-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="e5152-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5152-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5152-105">フォームからの通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="e5152-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5152-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e5152-106">Header file:</span></span>  <br/> |<span data-ttu-id="e5152-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e5152-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e5152-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="e5152-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e5152-109">シンク オブジェクトをビューに伝えます。</span><span class="sxs-lookup"><span data-stu-id="e5152-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="e5152-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e5152-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5152-111">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="e5152-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="e5152-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e5152-112">Called by:</span></span>  <br/> |<span data-ttu-id="e5152-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="e5152-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="e5152-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="e5152-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e5152-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e5152-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="e5152-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="e5152-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e5152-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="e5152-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e5152-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e5152-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e5152-119">に</span><span class="sxs-lookup"><span data-stu-id="e5152-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="e5152-120">フォーム ビューアーに、フォームが閉じられることを通知します。</span><span class="sxs-lookup"><span data-stu-id="e5152-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="e5152-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="e5152-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="e5152-122">新規または既存のメッセージのいずれかに読み込まれました、フォーム、フォームのビューアーを通知します。</span><span class="sxs-lookup"><span data-stu-id="e5152-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="e5152-123">印刷時</span><span class="sxs-lookup"><span data-stu-id="e5152-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="e5152-124">フォーム ビューアーのフォームの印刷の状態を通知します。</span><span class="sxs-lookup"><span data-stu-id="e5152-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="e5152-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="e5152-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="e5152-126">フォーム ビューアーの現在のメッセージが MAPI スプーラーに送信されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="e5152-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="e5152-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="e5152-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="e5152-128">フォームの現在のメッセージが保存されているフォーム ビューアーを通知します。</span><span class="sxs-lookup"><span data-stu-id="e5152-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5152-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5152-129">See also</span></span>



[<span data-ttu-id="e5152-130">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e5152-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

