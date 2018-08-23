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
ms.openlocfilehash: cee58299147c9f97ff61a3b8c460125349910637
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594461"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="54d32-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54d32-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="54d32-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54d32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54d32-105">フォームの閲覧者から通知を受信するフォームのサーバーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="54d32-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54d32-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="54d32-106">Header file:</span></span>  <br/> |<span data-ttu-id="54d32-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="54d32-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="54d32-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="54d32-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="54d32-109">シンク オブジェクトをフォームに伝えます。</span><span class="sxs-lookup"><span data-stu-id="54d32-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="54d32-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="54d32-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="54d32-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="54d32-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="54d32-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="54d32-112">Called by:</span></span>  <br/> |<span data-ttu-id="54d32-113">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="54d32-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="54d32-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="54d32-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="54d32-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="54d32-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="54d32-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="54d32-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="54d32-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="54d32-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="54d32-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="54d32-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="54d32-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="54d32-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="54d32-120">フォーム ビューアーのステータスに変更が発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="54d32-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="54d32-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="54d32-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="54d32-122">フォームを表示するのには、次のメッセージのメッセージ クラスを処理できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="54d32-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54d32-123">注釈</span><span class="sxs-lookup"><span data-stu-id="54d32-123">Remarks</span></span>

<span data-ttu-id="54d32-124">フォーム、フォームのサーバーの使用は、そのフォーム オブジェクトに含めての代わりに**IMAPIFormAdviseSink**を実装するシンク オブジェクトを案内します。</span><span class="sxs-lookup"><span data-stu-id="54d32-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="54d32-125">したがって、フォームの閲覧者はこのインターフェイスへのポインターを取得するフォームの[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)メソッドに失敗した呼び出しを想定します。</span><span class="sxs-lookup"><span data-stu-id="54d32-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="54d32-126">フォーム サーバーでは、通知を登録するのには、ビューアーの[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="54d32-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="54d32-127">**IMAPIFormAdviseSink**実装へのポインターでは、パラメーターとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="54d32-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54d32-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="54d32-128">See also</span></span>



[<span data-ttu-id="54d32-129">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="54d32-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

