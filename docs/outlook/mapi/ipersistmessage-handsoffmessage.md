---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fd7e3b1d1284cdf4451330aabcce8fd0279ad5ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801108"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="59312-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="59312-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="59312-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59312-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59312-105">フォームの現在のメッセージを解放するが発生します。</span><span class="sxs-lookup"><span data-stu-id="59312-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="59312-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="59312-106">Parameters</span></span>

<span data-ttu-id="59312-107">なし</span><span class="sxs-lookup"><span data-stu-id="59312-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="59312-108">�߂�l</span><span class="sxs-lookup"><span data-stu-id="59312-108">Return value</span></span>

<span data-ttu-id="59312-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="59312-109">S_OK</span></span> 
  
> <span data-ttu-id="59312-110">メッセージは正常にリリースされました。</span><span class="sxs-lookup"><span data-stu-id="59312-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59312-111">注釈</span><span class="sxs-lookup"><span data-stu-id="59312-111">Remarks</span></span>

<span data-ttu-id="59312-112">HandsOff の 2 つの状態への移行をフォームします。</span><span class="sxs-lookup"><span data-stu-id="59312-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="59312-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="59312-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="59312-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="59312-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="59312-115">フォームは、これらの状態のいずれかの方法では、永続的に保存されているとします。</span><span class="sxs-lookup"><span data-stu-id="59312-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="59312-116">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="59312-116">Notes to implementers</span></span>

<span data-ttu-id="59312-117">メッセージごとに再帰的に呼び出し**HandsOffMessage**が、現在のメッセージと、[に埋め込まれたフォーム ビューアーは、フォームが[標準](normal-state.md)または[NoScribble](noscribble-state.md)の状態にあるときに、 **IPersistMessage::HandsOffMessage**メソッドを呼び出すとIPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)各 OLE オブジェクトのメソッドは、現在のメッセージに埋め込まれています。</span><span class="sxs-lookup"><span data-stu-id="59312-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="59312-118">現在のメッセージとメッセージのすべての埋め込み OLE オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="59312-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="59312-119">通常の状態で、フォームがあった場合は、HandsOffFromNormal 状態に移行します。</span><span class="sxs-lookup"><span data-stu-id="59312-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="59312-120">NoScribble 状態で、フォームがあった場合は、HandsOffAfterSave 状態に移行します。</span><span class="sxs-lookup"><span data-stu-id="59312-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="59312-121">移行に成功した後メッセージ[が](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出すし、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="59312-121">After a successful transition, call the message's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="59312-122">フォーム ビューアーは、HandsOff 状態のいずれかの方法では、フォーム中に**HandsOffMessage**を呼び出す、ときに E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="59312-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="59312-123">フォームのさまざまな状態の詳細については、[フォームの状態](form-states.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="59312-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="59312-124">HandsOff 状態のストレージ ・ オブジェクトを操作する方法の詳細については、 [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="59312-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59312-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="59312-125">See also</span></span>



[<span data-ttu-id="59312-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="59312-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="59312-127">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="59312-127">Form States</span></span>](form-states.md)

