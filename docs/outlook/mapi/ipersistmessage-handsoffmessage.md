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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309717"
---
# <a name="ipersistmessagehandsoffmessage"></a><span data-ttu-id="f08e7-103">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="f08e7-103">IPersistMessage::HandsOffMessage</span></span>

  
  
<span data-ttu-id="f08e7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f08e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f08e7-105">フォームが現在のメッセージを解放します。</span><span class="sxs-lookup"><span data-stu-id="f08e7-105">Causes the form to release its current message.</span></span>
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="f08e7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f08e7-106">Parameters</span></span>

<span data-ttu-id="f08e7-107">なし</span><span class="sxs-lookup"><span data-stu-id="f08e7-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f08e7-108">戻り値</span><span class="sxs-lookup"><span data-stu-id="f08e7-108">Return value</span></span>

<span data-ttu-id="f08e7-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="f08e7-109">S_OK</span></span> 
  
> <span data-ttu-id="f08e7-110">メッセージが正常にリリースされました。</span><span class="sxs-lookup"><span data-stu-id="f08e7-110">The message was successfully released.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f08e7-111">注釈</span><span class="sxs-lookup"><span data-stu-id="f08e7-111">Remarks</span></span>

<span data-ttu-id="f08e7-112">フォームは 2 つの HandsOff 状態に移行します。</span><span class="sxs-lookup"><span data-stu-id="f08e7-112">Forms transition into two HandsOff states:</span></span>
  
- [<span data-ttu-id="f08e7-113">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="f08e7-113">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="f08e7-114">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="f08e7-114">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="f08e7-115">フォームがいずれかの状態にある場合、フォームは永続的に保存されているプロセスです。</span><span class="sxs-lookup"><span data-stu-id="f08e7-115">When a form is in either of these states, it is in the process of being stored permanently.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f08e7-116">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f08e7-116">Notes to implementers</span></span>

<span data-ttu-id="f08e7-117">フォーム ビューアーが **IPersistMessage::HandsOffMessage** メソッドを呼び出す場合 [](normal-state.md)、フォームが Normal または [NoScribble](noscribble-state.md)状態のときに、現在のメッセージに埋め込まれている各メッセージで **HandsOffMessage** を再帰的に呼び出し、現在のメッセージに埋め込まれている各 OLE オブジェクトの [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f08e7-117">When a form viewer calls the **IPersistMessage::HandsOffMessage** method while your form is in the [Normal](normal-state.md) or [NoScribble](noscribble-state.md) state, recursively call **HandsOffMessage** on each message embedded in the current message and the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method on each OLE object embedded in the current message.</span></span> <span data-ttu-id="f08e7-118">次に、現在のメッセージとすべての埋め込みメッセージと OLE オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="f08e7-118">Then release the current message and all embedded messages and OLE objects.</span></span> <span data-ttu-id="f08e7-119">フォームが Normal 状態の場合は、HandsOffFromNormal 状態に移行します。</span><span class="sxs-lookup"><span data-stu-id="f08e7-119">If your form was in the Normal state, transition to the HandsOffFromNormal state.</span></span> <span data-ttu-id="f08e7-120">フォームが NoScribble 状態の場合は、HandsOffAfterSave 状態に移行します。</span><span class="sxs-lookup"><span data-stu-id="f08e7-120">If your form was in the NoScribble state, transition to the HandsOffAfterSave state.</span></span> <span data-ttu-id="f08e7-121">移行が成功したら、メッセージの [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) メソッドを呼び出し、S_OK。</span><span class="sxs-lookup"><span data-stu-id="f08e7-121">After a successful transition, call the message's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method and return S_OK.</span></span> 
  
<span data-ttu-id="f08e7-122">フォームビューアーが **HandsOffMessage を呼び出** し、フォームがいずれかの HandsOff 状態にある場合は、次のE_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="f08e7-122">When a form viewer calls **HandsOffMessage** while your form is in either of the HandsOff states, return E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="f08e7-123">フォームの異なる状態の詳細については、「フォームの状態」 [を参照してください](form-states.md)。</span><span class="sxs-lookup"><span data-stu-id="f08e7-123">For more information about the different states of a form, see [Form States](form-states.md).</span></span> <span data-ttu-id="f08e7-124">ストレージ オブジェクトの HandsOff 状態を操作する方法の詳細については [、「IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) メソッド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f08e7-124">For more information about how to work with the HandsOff state of storage objects, see the [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f08e7-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="f08e7-125">See also</span></span>



[<span data-ttu-id="f08e7-126">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f08e7-126">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="f08e7-127">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="f08e7-127">Form States</span></span>](form-states.md)

