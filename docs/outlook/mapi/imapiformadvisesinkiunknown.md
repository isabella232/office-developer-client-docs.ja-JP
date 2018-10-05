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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392061"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="3f00e-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f00e-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="3f00e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f00e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f00e-105">フォームの閲覧者から通知を受信するフォームのサーバーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f00e-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f00e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3f00e-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f00e-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="3f00e-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="3f00e-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="3f00e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3f00e-109">シンク オブジェクトをフォームに伝えます。</span><span class="sxs-lookup"><span data-stu-id="3f00e-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="3f00e-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="3f00e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f00e-111">フォーム サーバー</span><span class="sxs-lookup"><span data-stu-id="3f00e-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="3f00e-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3f00e-112">Called by:</span></span>  <br/> |<span data-ttu-id="3f00e-113">フォームの閲覧者</span><span class="sxs-lookup"><span data-stu-id="3f00e-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="3f00e-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="3f00e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3f00e-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3f00e-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="3f00e-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="3f00e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3f00e-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="3f00e-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3f00e-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="3f00e-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3f00e-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="3f00e-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="3f00e-120">フォーム ビューアーのステータスに変更が発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="3f00e-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="3f00e-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="3f00e-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="3f00e-122">フォームを表示するのには、次のメッセージのメッセージ クラスを処理できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="3f00e-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f00e-123">備考</span><span class="sxs-lookup"><span data-stu-id="3f00e-123">Remarks</span></span>

<span data-ttu-id="3f00e-124">フォーム、フォームのサーバーの使用は、そのフォーム オブジェクトに含めての代わりに**IMAPIFormAdviseSink**を実装するシンク オブジェクトを案内します。</span><span class="sxs-lookup"><span data-stu-id="3f00e-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="3f00e-125">したがって、フォームの閲覧者はこのインターフェイスへのポインターを取得するフォームの[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドに失敗した呼び出しを想定します。</span><span class="sxs-lookup"><span data-stu-id="3f00e-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="3f00e-126">フォーム サーバーでは、通知を登録するのには、ビューアーの[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3f00e-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="3f00e-127">**IMAPIFormAdviseSink**実装へのポインターでは、パラメーターとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="3f00e-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f00e-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f00e-128">See also</span></span>



[<span data-ttu-id="3f00e-129">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3f00e-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

