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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429419"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="c4178-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4178-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="c4178-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4178-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4178-105">フォームから通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="c4178-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4178-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c4178-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4178-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="c4178-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="c4178-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="c4178-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c4178-109">シンク オブジェクトの表示</span><span class="sxs-lookup"><span data-stu-id="c4178-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="c4178-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="c4178-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4178-111">フォーム ビューアー</span><span class="sxs-lookup"><span data-stu-id="c4178-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="c4178-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c4178-112">Called by:</span></span>  <br/> |<span data-ttu-id="c4178-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c4178-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="c4178-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="c4178-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c4178-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c4178-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="c4178-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="c4178-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c4178-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="c4178-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c4178-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="c4178-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c4178-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="c4178-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="c4178-120">フォームが閉じているとフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c4178-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="c4178-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="c4178-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="c4178-122">新しいメッセージまたは既存のメッセージがフォームに読み込まれたとフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c4178-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="c4178-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="c4178-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="c4178-124">フォームの印刷状態をフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c4178-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="c4178-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="c4178-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="c4178-126">現在のメッセージが MAPI スプーラーに送信されたとフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c4178-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="c4178-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="c4178-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="c4178-128">フォームの現在のメッセージが保存されたとフォーム ビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="c4178-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4178-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4178-129">See also</span></span>



[<span data-ttu-id="c4178-130">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="c4178-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

