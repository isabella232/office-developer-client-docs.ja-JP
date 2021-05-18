---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406032"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="e3cbe-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3cbe-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="e3cbe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3cbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3cbe-105">クライアント アプリケーションのフォーム ビューアーでフォームを管理します。</span><span class="sxs-lookup"><span data-stu-id="e3cbe-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3cbe-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e3cbe-106">Header file:</span></span>  <br/> |<span data-ttu-id="e3cbe-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e3cbe-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e3cbe-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="e3cbe-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e3cbe-109">コンテキスト オブジェクトの表示</span><span class="sxs-lookup"><span data-stu-id="e3cbe-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="e3cbe-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="e3cbe-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e3cbe-111">フォーム ビューアー</span><span class="sxs-lookup"><span data-stu-id="e3cbe-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="e3cbe-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e3cbe-112">Called by:</span></span>  <br/> |<span data-ttu-id="e3cbe-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="e3cbe-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="e3cbe-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="e3cbe-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e3cbe-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="e3cbe-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="e3cbe-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="e3cbe-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e3cbe-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="e3cbe-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e3cbe-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e3cbe-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e3cbe-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e3cbe-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="e3cbe-120">フォームの登録を管理して、ビューアーの変更に関する通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="e3cbe-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="e3cbe-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="e3cbe-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="e3cbe-122">フォーム ビューアーで次または前のメッセージをアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="e3cbe-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="e3cbe-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="e3cbe-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="e3cbe-124">現在の印刷情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="e3cbe-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="e3cbe-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="e3cbe-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="e3cbe-126">現在のメッセージの保存に使用するストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="e3cbe-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="e3cbe-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="e3cbe-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="e3cbe-128">現在のビューアーの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="e3cbe-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="e3cbe-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e3cbe-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="e3cbe-130">ビュー コンテキスト オブジェクトで発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="e3cbe-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3cbe-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3cbe-131">See also</span></span>



[<span data-ttu-id="e3cbe-132">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="e3cbe-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

