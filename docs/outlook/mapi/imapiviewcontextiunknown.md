---
title: imapiviewcontext IUnknown
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351138"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="7efba-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7efba-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="7efba-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7efba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7efba-105">クライアントアプリケーションのフォームビューアーでフォームを管理します。</span><span class="sxs-lookup"><span data-stu-id="7efba-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7efba-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7efba-106">Header file:</span></span>  <br/> |<span data-ttu-id="7efba-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="7efba-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7efba-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="7efba-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7efba-109">コンテキストオブジェクトを表示する</span><span class="sxs-lookup"><span data-stu-id="7efba-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="7efba-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="7efba-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7efba-111">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="7efba-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="7efba-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="7efba-112">Called by:</span></span>  <br/> |<span data-ttu-id="7efba-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7efba-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="7efba-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="7efba-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7efba-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="7efba-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="7efba-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="7efba-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7efba-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="7efba-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7efba-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="7efba-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7efba-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="7efba-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="7efba-120">フォームの登録を管理して、閲覧者の変更に関する通知を受信します。</span><span class="sxs-lookup"><span data-stu-id="7efba-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="7efba-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="7efba-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="7efba-122">フォームビューアーで次または前のメッセージをアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="7efba-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="7efba-123">getprintsetup</span><span class="sxs-lookup"><span data-stu-id="7efba-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="7efba-124">現在の印刷情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="7efba-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="7efba-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="7efba-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="7efba-126">現在のメッセージを保存するために使用するストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="7efba-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="7efba-127">getviewstatus</span><span class="sxs-lookup"><span data-stu-id="7efba-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="7efba-128">現在のビューアーの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="7efba-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="7efba-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="7efba-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="7efba-130">ビューコンテキストオブジェクトで発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="7efba-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7efba-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="7efba-131">See also</span></span>



[<span data-ttu-id="7efba-132">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="7efba-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

