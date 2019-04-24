---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317137"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="ea3de-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="ea3de-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="ea3de-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea3de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea3de-105">保存操作が完了したことをフォームに通知します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="ea3de-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ea3de-106">Parameters</span></span>

<span data-ttu-id="ea3de-107">_pmessage_</span><span class="sxs-lookup"><span data-stu-id="ea3de-107">_pMessage_</span></span>
  
> <span data-ttu-id="ea3de-108">順番新しく保存されたメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ea3de-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ea3de-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="ea3de-109">Return value</span></span>

<span data-ttu-id="ea3de-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea3de-110">S_OK</span></span> 
  
> <span data-ttu-id="ea3de-111">通知は正常に実行されました。</span><span class="sxs-lookup"><span data-stu-id="ea3de-111">The notification was successful.</span></span>
    
<span data-ttu-id="ea3de-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ea3de-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="ea3de-113">_pmessage_パラメーターが NULL で、フォームは、[標準] または [[標準](handsofffromnormal-state.md)] [[保存](handsoffaftersave-state.md)の状態] のどちらかです。</span><span class="sxs-lookup"><span data-stu-id="ea3de-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="ea3de-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="ea3de-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="ea3de-115">フォームが次のいずれかの状態になっていません。</span><span class="sxs-lookup"><span data-stu-id="ea3de-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="ea3de-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="ea3de-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="ea3de-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="ea3de-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="ea3de-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="ea3de-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="ea3de-119">解説</span><span class="sxs-lookup"><span data-stu-id="ea3de-119">Remarks</span></span>

<span data-ttu-id="ea3de-120">**IPersistMessage:: SaveCompleted**メソッドは、すべての保留中の変更が保存されたことをフォームに通知するためにフォームビューアーによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ea3de-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="ea3de-121">**SaveCompleted**は、フォームが次のいずれかの状態にある場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea3de-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="ea3de-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="ea3de-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="ea3de-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="ea3de-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="ea3de-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="ea3de-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="ea3de-125">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="ea3de-125">Notes to implementers</span></span>

<span data-ttu-id="ea3de-126">**SaveCompleted**メソッドが実行できるアクションには、メッセージポインターパラメーターに含まれる内容と、メッセージの状態によっていくつかあります。</span><span class="sxs-lookup"><span data-stu-id="ea3de-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="ea3de-127">ただし、正常に処理された場合は、 _pmessage_パラメーターが参照しているメッセージの現在の状態を常に保存し、フォームを[通常](normal-state.md)の状態に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="ea3de-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="ea3de-128">次の表では、 **SaveCompleted**の実装で実行する必要がある処理に影響する条件について説明します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="ea3de-129">**条件**</span><span class="sxs-lookup"><span data-stu-id="ea3de-129">**Condition**</span></span>|<span data-ttu-id="ea3de-130">**処理**</span><span class="sxs-lookup"><span data-stu-id="ea3de-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea3de-131">_pmessage_パラメーターが NULL で、 [IPersistMessage:: Save](ipersistmessage-save.md)メソッドの_fsameasload_パラメーターが TRUE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ea3de-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="ea3de-132">登録されているすべてのビューアーの[IMAPIViewAdviseSink:: onsaved](imapiviewadvisesink-onsaved.md)メソッドを呼び出し、フォームをクリーンとしてマークし、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ea3de-133">_pmessage_パラメーターが NULL で、 **IPersistMessage:: Save**メソッドの_fsameasload_パラメーターが FALSE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ea3de-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="ea3de-134">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="ea3de-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ea3de-135">フォームは、[標準時の標準状態にあります。</span><span class="sxs-lookup"><span data-stu-id="ea3de-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="ea3de-136">現在のメッセージを解放し、 _pmessage_パラメーターで示されるメッセージに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ea3de-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="ea3de-137">置換メッセージの[IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出し、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ea3de-138">フォームは、[保存の状態にあります。</span><span class="sxs-lookup"><span data-stu-id="ea3de-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="ea3de-139">登録されているすべてのビューアーの**IMAPIViewAdviseSink:: onsaved**メソッドを呼び出し、フォームをクリーンとしてマークし、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ea3de-140">フォームは、 [noscribble](noscribble-state.md)状態にあります。</span><span class="sxs-lookup"><span data-stu-id="ea3de-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="ea3de-141">現在のメッセージを解放し、それを_pmessage_で示されるメッセージに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ea3de-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="ea3de-142">置換メッセージの**IUnknown:: AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="ea3de-143">登録されているすべてのビューアーの**IMAPIViewAdviseSink:: onsaved**メソッドを呼び出し、フォームをクリーンとしてマークし、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ea3de-144">フォームは HandsOff 状態のいずれかで、 _pmessage_パラメーターが NULL に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ea3de-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="ea3de-145">E_INVALIDARG を返します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="ea3de-146">フォームは、HandsOff 状態または noscribble 状態のいずれでもない状態にあります。</span><span class="sxs-lookup"><span data-stu-id="ea3de-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="ea3de-147">E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="ea3de-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="ea3de-148">ストレージオブジェクトの保存の詳細については、 [IPersistStorage:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted)メソッドまたは[IPersistFile:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted)メソッドのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea3de-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ea3de-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea3de-149">See also</span></span>

- [<span data-ttu-id="ea3de-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea3de-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="ea3de-151">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="ea3de-151">Form States</span></span>](form-states.md)
