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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7a82ce9a46017993adfc6c4c755b6c97b847e579
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801125"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="4a753-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="4a753-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="4a753-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a753-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a753-105">フォームに通知する、保存操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="4a753-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="4a753-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4a753-106">Parameters</span></span>

<span data-ttu-id="4a753-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="4a753-107">_pMessage_</span></span>
  
> <span data-ttu-id="4a753-108">[in]新しく保存されたメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4a753-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a753-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4a753-109">Return value</span></span>

<span data-ttu-id="4a753-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a753-110">S_OK</span></span> 
  
> <span data-ttu-id="4a753-111">通知が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="4a753-111">The notification was successful.</span></span>
    
<span data-ttu-id="4a753-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4a753-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="4a753-113">_PMessage_パラメーターが NULL と、フォームは、 [HandsOffFromNormal](handsofffromnormal-state.md)または[HandsOffAfterSave](handsoffaftersave-state.md)の状態のいずれかの方法です。</span><span class="sxs-lookup"><span data-stu-id="4a753-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="4a753-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="4a753-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="4a753-115">状態は、次のいずれかのフォームではありません。</span><span class="sxs-lookup"><span data-stu-id="4a753-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="4a753-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="4a753-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="4a753-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="4a753-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="4a753-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="4a753-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="4a753-119">備考</span><span class="sxs-lookup"><span data-stu-id="4a753-119">Remarks</span></span>

<span data-ttu-id="4a753-120">**IPersistMessage::SaveCompleted**メソッドは、すべての保留中の変更が保存されているフォームを通知するためにフォーム ビューアーによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4a753-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="4a753-121">**SaveCompleted**は、フォームが次の状態のいずれかの場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a753-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="4a753-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="4a753-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="4a753-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="4a753-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="4a753-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="4a753-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="4a753-125">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="4a753-125">Notes to implementers</span></span>

<span data-ttu-id="4a753-126">**SaveCompleted**メソッドを実行できるいくつかの実行可能なアクションがある、どのようなメッセージによっては、ポインター パラメーターが含まれるとのメッセージではどのような状態。</span><span class="sxs-lookup"><span data-stu-id="4a753-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="4a753-127">ただし、アクションが成功すると、常にフォームを保存_pMessage_パラメーターが指すメッセージと切り替えの現在の状態の[通常](normal-state.md)の状態にします。</span><span class="sxs-lookup"><span data-stu-id="4a753-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="4a753-128">次の表では、 **SaveCompleted**の実装で実行する必要があります操作に影響を与える条件について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a753-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="4a753-129">**条件**</span><span class="sxs-lookup"><span data-stu-id="4a753-129">**Condition**</span></span>|<span data-ttu-id="4a753-130">**アクション**</span><span class="sxs-lookup"><span data-stu-id="4a753-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a753-131">_PMessage_パラメーターが NULL と[IPersistMessage::Save](ipersistmessage-save.md)メソッドの_fSameAsLoad_パラメーターが TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="4a753-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="4a753-132">すべての登録されているビューアーの[IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md)メソッドを呼び出して、フォーム、および戻り値 S_OK としてマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="4a753-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="4a753-133">_PMessage_パラメーターが NULL と**IPersistMessage::Save**メソッドの_fSameAsLoad_パラメーターが FALSE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="4a753-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="4a753-134">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="4a753-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="4a753-135">フォームでは、HandsOffFromNormal 状態にします。</span><span class="sxs-lookup"><span data-stu-id="4a753-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="4a753-136">現在のメッセージを解放し、 _pMessage_パラメーターで指定されたメッセージに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="4a753-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="4a753-137">交換メッセージの[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出すし、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="4a753-137">Call the replacement message's [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="4a753-138">フォームでは、HandsOffAfterSave 状態にします。</span><span class="sxs-lookup"><span data-stu-id="4a753-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="4a753-139">すべての登録されているビューアーの**IMAPIViewAdviseSink::OnSaved**メソッドを呼び出して、フォーム、および戻り値 S_OK としてマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="4a753-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="4a753-140">フォームでは、 [NoScribble](noscribble-state.md)状態にします。</span><span class="sxs-lookup"><span data-stu-id="4a753-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="4a753-141">現在のメッセージを解放し、 _pMessage_に示されるメッセージに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="4a753-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="4a753-142">交換メッセージの**IUnknown::AddRef**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4a753-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="4a753-143">すべての登録されているビューアーの**IMAPIViewAdviseSink::OnSaved**メソッドを呼び出して、フォーム、および戻り値 S_OK としてマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="4a753-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="4a753-144">HandsOff 状態のいずれかでは、フォームと_pMessage_パラメーターは NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="4a753-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="4a753-145">E_INVALIDARG を返します。</span><span class="sxs-lookup"><span data-stu-id="4a753-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="4a753-146">フォーム以外 HandsOff 状態のいずれかの状態または状態にある、NoScribble です。</span><span class="sxs-lookup"><span data-stu-id="4a753-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="4a753-147">E_UNEXPECTED が返されます。</span><span class="sxs-lookup"><span data-stu-id="4a753-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="4a753-148">ストレージ ・ オブジェクトを保存する方法の詳細については、 [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx)または[IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx)のメソッドのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a753-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) or [IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a753-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a753-149">See also</span></span>



[<span data-ttu-id="4a753-150">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a753-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="4a753-151">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="4a753-151">Form States</span></span>](form-states.md)


[<span data-ttu-id="4a753-152">IPersistStorage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="4a753-152">IPersistStorage::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx)
  
[<span data-ttu-id="4a753-153">IPersistFile::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="4a753-153">IPersistFile::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx)

