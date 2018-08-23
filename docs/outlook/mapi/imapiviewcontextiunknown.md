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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ae2729ec5620b6b408a5c999d4b6ede7143bed2f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584567"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="8afaf-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8afaf-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="8afaf-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8afaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8afaf-105">クライアント アプリケーションのフォームのビューアーでフォームを管理します。</span><span class="sxs-lookup"><span data-stu-id="8afaf-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8afaf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8afaf-106">Header file:</span></span>  <br/> |<span data-ttu-id="8afaf-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="8afaf-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8afaf-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="8afaf-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8afaf-109">コンテキスト オブジェクトの表示</span><span class="sxs-lookup"><span data-stu-id="8afaf-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="8afaf-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="8afaf-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8afaf-111">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="8afaf-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="8afaf-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8afaf-112">Called by:</span></span>  <br/> |<span data-ttu-id="8afaf-113">フォーム オブジェクト</span><span class="sxs-lookup"><span data-stu-id="8afaf-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="8afaf-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="8afaf-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8afaf-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="8afaf-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="8afaf-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="8afaf-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8afaf-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="8afaf-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8afaf-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="8afaf-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8afaf-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8afaf-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="8afaf-120">ビューアーの変更についての通知を受信するフォームの登録を管理します。</span><span class="sxs-lookup"><span data-stu-id="8afaf-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="8afaf-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="8afaf-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="8afaf-122">フォーム ビューアー内の次または前のメッセージをアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="8afaf-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="8afaf-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="8afaf-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="8afaf-124">現在、印刷情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="8afaf-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="8afaf-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="8afaf-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="8afaf-126">現在のメッセージを保存するために使用するストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="8afaf-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="8afaf-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="8afaf-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="8afaf-128">ビューアーの現在の状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="8afaf-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="8afaf-129">発生しました</span><span class="sxs-lookup"><span data-stu-id="8afaf-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="8afaf-130">前のビューのコンテキスト内で発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="8afaf-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8afaf-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="8afaf-131">See also</span></span>



[<span data-ttu-id="8afaf-132">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8afaf-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

