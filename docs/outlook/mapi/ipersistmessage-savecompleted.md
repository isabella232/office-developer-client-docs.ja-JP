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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317137"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="02cff-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="02cff-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="02cff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02cff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02cff-105">保存操作が完了したフォームに通知します。</span><span class="sxs-lookup"><span data-stu-id="02cff-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="02cff-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="02cff-106">Parameters</span></span>

<span data-ttu-id="02cff-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="02cff-107">_pMessage_</span></span>
  
> <span data-ttu-id="02cff-108">[in]新しく保存されたメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="02cff-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="02cff-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="02cff-109">Return value</span></span>

<span data-ttu-id="02cff-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="02cff-110">S_OK</span></span> 
  
> <span data-ttu-id="02cff-111">通知が成功しました。</span><span class="sxs-lookup"><span data-stu-id="02cff-111">The notification was successful.</span></span>
    
<span data-ttu-id="02cff-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="02cff-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="02cff-113">_pMessage パラメーター_ は NULL で、フォームは [HandsOffFromNormal](handsofffromnormal-state.md)または [HandsOffAfterSave](handsoffaftersave-state.md)状態のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="02cff-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="02cff-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="02cff-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="02cff-115">フォームは、次のいずれかの状態ではありません。</span><span class="sxs-lookup"><span data-stu-id="02cff-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="02cff-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="02cff-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="02cff-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="02cff-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="02cff-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="02cff-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="02cff-119">注釈</span><span class="sxs-lookup"><span data-stu-id="02cff-119">Remarks</span></span>

<span data-ttu-id="02cff-120">**IPersistMessage::SaveCompleted** メソッドは、フォーム ビューアーによって呼び出され、保留中のすべての変更が保存されたというフォームを通知します。</span><span class="sxs-lookup"><span data-stu-id="02cff-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="02cff-121">**SaveCompleted は** 、フォームが次のいずれかの状態にある場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="02cff-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="02cff-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="02cff-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="02cff-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="02cff-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="02cff-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="02cff-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="02cff-125">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="02cff-125">Notes to implementers</span></span>

<span data-ttu-id="02cff-126">**SaveCompleted** メソッドが実行できるアクションは、メッセージ ポインター パラメーターに含まれるもの、およびメッセージの状態に応じていくつか考えられる操作です。</span><span class="sxs-lookup"><span data-stu-id="02cff-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="02cff-127">ただし、アクションが成功した場合は  _、pMessage_ パラメーターがポイントするメッセージの現在の状態を常に保存し、フォームを標準状態 [に移行](normal-state.md) します。</span><span class="sxs-lookup"><span data-stu-id="02cff-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="02cff-128">次の表に **、SaveCompleted** の実装で実行する必要があるアクションに影響を与える条件を示します。</span><span class="sxs-lookup"><span data-stu-id="02cff-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="02cff-129">**条件**</span><span class="sxs-lookup"><span data-stu-id="02cff-129">**Condition**</span></span>|<span data-ttu-id="02cff-130">**処理**</span><span class="sxs-lookup"><span data-stu-id="02cff-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02cff-131">_pMessage パラメーター_ は NULL で [、IPersistMessage::Save](ipersistmessage-save.md)メソッドの _fSameAsLoad_ パラメーターは TRUE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="02cff-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="02cff-132">すべての登録済 [みビューアーの IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) メソッドを呼び出し、フォームをクリーンとしてマークし、フォームを戻S_OK。</span><span class="sxs-lookup"><span data-stu-id="02cff-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="02cff-133">_pMessage パラメーター_ は NULL で **、IPersistMessage::Save** メソッドの _fSameAsLoad_ パラメーターは FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="02cff-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="02cff-134">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="02cff-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="02cff-135">フォームは HandsOffFromNormal 状態です。</span><span class="sxs-lookup"><span data-stu-id="02cff-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="02cff-136">現在のメッセージを解放し、pMessage パラメーターが指すメッセージ  _に置き換_ える。</span><span class="sxs-lookup"><span data-stu-id="02cff-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="02cff-137">置換メッセージの [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) メソッドを呼び出し、次のS_OK。</span><span class="sxs-lookup"><span data-stu-id="02cff-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="02cff-138">フォームは HandsOffAfterSave 状態です。</span><span class="sxs-lookup"><span data-stu-id="02cff-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="02cff-139">すべての登録済 **みビューアーの IMAPIViewAdviseSink::OnSaved** メソッドを呼び出し、フォームをクリーンとしてマークし、フォームを戻S_OK。</span><span class="sxs-lookup"><span data-stu-id="02cff-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="02cff-140">フォームは [NoScribble 状態](noscribble-state.md) です。</span><span class="sxs-lookup"><span data-stu-id="02cff-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="02cff-141">現在のメッセージを解放し、pMessage が指すメッセージに  _置き換える_。</span><span class="sxs-lookup"><span data-stu-id="02cff-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="02cff-142">置換メッセージの **IUnknown::AddRef メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="02cff-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="02cff-143">すべての登録済 **みビューアーの IMAPIViewAdviseSink::OnSaved** メソッドを呼び出し、フォームをクリーンとしてマークし、フォームを戻S_OK。</span><span class="sxs-lookup"><span data-stu-id="02cff-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="02cff-144">フォームは HandsOff 状態の 1 つで  _、pMessage_ パラメーターは NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="02cff-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="02cff-145">値をE_INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="02cff-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="02cff-146">フォームは、HandsOff 状態または NoScribble 状態以外の状態です。</span><span class="sxs-lookup"><span data-stu-id="02cff-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="02cff-147">値をE_UNEXPECTED。</span><span class="sxs-lookup"><span data-stu-id="02cff-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="02cff-148">ストレージ オブジェクトの保存の詳細については [、IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) メソッドまたは [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) メソッドのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="02cff-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02cff-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="02cff-149">See also</span></span>

- [<span data-ttu-id="02cff-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02cff-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="02cff-151">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="02cff-151">Form States</span></span>](form-states.md)
