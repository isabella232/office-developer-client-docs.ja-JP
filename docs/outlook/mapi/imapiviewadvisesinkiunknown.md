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
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351141"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="3b3e2-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b3e2-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="3b3e2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b3e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b3e2-105">フォームから通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="3b3e2-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b3e2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3b3e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b3e2-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="3b3e2-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="3b3e2-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="3b3e2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3b3e2-109">アドバイズシンクオブジェクトの表示</span><span class="sxs-lookup"><span data-stu-id="3b3e2-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="3b3e2-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="3b3e2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3b3e2-111">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="3b3e2-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="3b3e2-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3b3e2-112">Called by:</span></span>  <br/> |<span data-ttu-id="3b3e2-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3b3e2-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="3b3e2-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="3b3e2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3b3e2-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3b3e2-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="3b3e2-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="3b3e2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3b3e2-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="3b3e2-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3b3e2-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="3b3e2-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3b3e2-119">onshutdown</span><span class="sxs-lookup"><span data-stu-id="3b3e2-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="3b3e2-120">フォームが閉じられていることをフォームビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="3b3e2-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="3b3e2-121">onnewmessage</span><span class="sxs-lookup"><span data-stu-id="3b3e2-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="3b3e2-122">フォームビューアーに、新規または既存のメッセージがフォームにロードされたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="3b3e2-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="3b3e2-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="3b3e2-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="3b3e2-124">フォームの印刷状態をフォームビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="3b3e2-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="3b3e2-125">onsubmitted</span><span class="sxs-lookup"><span data-stu-id="3b3e2-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="3b3e2-126">現在のメッセージが MAPI スプーラーに送信されたことをフォームビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="3b3e2-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="3b3e2-127">onsaved</span><span class="sxs-lookup"><span data-stu-id="3b3e2-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="3b3e2-128">フォームの現在のメッセージが保存されたことをフォームビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="3b3e2-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b3e2-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b3e2-129">See also</span></span>



[<span data-ttu-id="3b3e2-130">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="3b3e2-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

