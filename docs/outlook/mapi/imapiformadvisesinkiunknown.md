---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286605"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="585c9-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="585c9-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="585c9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="585c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="585c9-105">フォームサーバーがフォームビューアーから通知を受信できるようにします。</span><span class="sxs-lookup"><span data-stu-id="585c9-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="585c9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="585c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="585c9-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="585c9-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="585c9-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="585c9-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="585c9-109">Form アドバイズシンクオブジェクト</span><span class="sxs-lookup"><span data-stu-id="585c9-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="585c9-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="585c9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="585c9-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="585c9-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="585c9-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="585c9-112">Called by:</span></span>  <br/> |<span data-ttu-id="585c9-113">フォームビューアー</span><span class="sxs-lookup"><span data-stu-id="585c9-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="585c9-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="585c9-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="585c9-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="585c9-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="585c9-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="585c9-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="585c9-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="585c9-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="585c9-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="585c9-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="585c9-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="585c9-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="585c9-120">フォームビューアーの状態で変更が発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="585c9-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="585c9-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="585c9-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="585c9-122">フォームが次に表示されるメッセージのメッセージクラスを処理できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="585c9-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="585c9-123">解説</span><span class="sxs-lookup"><span data-stu-id="585c9-123">Remarks</span></span>

<span data-ttu-id="585c9-124">フォームサーバーは form アドバイズシンクオブジェクトを使用して、form オブジェクトに含めるのではなく、 **IMAPIFormAdviseSink**を実装します。</span><span class="sxs-lookup"><span data-stu-id="585c9-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="585c9-125">そのため、フォーム閲覧者は、このインターフェイスへのポインターを取得するために、フォームの[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドへの呼び出しが失敗したことを想定してください。</span><span class="sxs-lookup"><span data-stu-id="585c9-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="585c9-126">フォームサーバーは、通知を登録するために、ビューアーの[imapiviewcontext:: SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="585c9-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="585c9-127">**IMAPIFormAdviseSink**実装へのポインターは、パラメーターとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="585c9-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="585c9-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="585c9-128">See also</span></span>



[<span data-ttu-id="585c9-129">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="585c9-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

