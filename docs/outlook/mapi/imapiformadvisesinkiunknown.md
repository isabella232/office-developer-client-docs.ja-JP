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
ms.openlocfilehash: fd2575d401aa8a39d6f3b2cd08377b587b430ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800517"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="00289-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00289-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="00289-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00289-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00289-105">フォームの閲覧者から通知を受信するフォームのサーバーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="00289-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00289-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="00289-106">Header file:</span></span>  <br/> |<span data-ttu-id="00289-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="00289-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="00289-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="00289-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="00289-109">シンク オブジェクトをフォームに伝えます。</span><span class="sxs-lookup"><span data-stu-id="00289-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="00289-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="00289-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="00289-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="00289-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="00289-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="00289-112">Called by:</span></span>  <br/> |<span data-ttu-id="00289-113">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="00289-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="00289-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="00289-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="00289-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="00289-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="00289-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="00289-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="00289-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="00289-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="00289-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="00289-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="00289-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="00289-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="00289-120">フォーム ビューアーのステータスに変更が発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="00289-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="00289-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="00289-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="00289-122">フォームを表示するのには、次のメッセージのメッセージ クラスを処理できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="00289-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00289-123">注釈</span><span class="sxs-lookup"><span data-stu-id="00289-123">Remarks</span></span>

<span data-ttu-id="00289-124">フォーム、フォームのサーバーの使用は、そのフォーム オブジェクトに含めての代わりに**IMAPIFormAdviseSink**を実装するシンク オブジェクトを案内します。</span><span class="sxs-lookup"><span data-stu-id="00289-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="00289-125">したがって、フォームの閲覧者はこのインターフェイスへのポインターを取得するフォームの[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)メソッドに失敗した呼び出しを想定します。</span><span class="sxs-lookup"><span data-stu-id="00289-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="00289-126">フォーム サーバーでは、通知を登録するのには、ビューアーの[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="00289-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="00289-127">**IMAPIFormAdviseSink**実装へのポインターでは、パラメーターとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="00289-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00289-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="00289-128">See also</span></span>



[<span data-ttu-id="00289-129">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="00289-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

