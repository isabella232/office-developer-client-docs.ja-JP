---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: eff192b0d2b5cde51a2909452b19ffe1a47b2c04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801114"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="07dbd-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="07dbd-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="07dbd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07dbd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07dbd-105">指定されたメッセージのフォームが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="07dbd-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="07dbd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="07dbd-106">Parameters</span></span>

 <span data-ttu-id="07dbd-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="07dbd-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="07dbd-108">[in]読み込まれるフォームのメッセージのサイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="07dbd-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="07dbd-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="07dbd-109">_pMessage_</span></span>
  
> <span data-ttu-id="07dbd-110">[in]フォームを読み込む必要があるメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="07dbd-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="07dbd-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="07dbd-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="07dbd-112">[in]メッセージの状態に関する情報を提供するメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティからコピーしたクライアント定義またはプロバイダー定義のフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="07dbd-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="07dbd-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="07dbd-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="07dbd-114">[in]メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティからコピーして、フラグのビットマスクを提供するさらに、メッセージの状態に関する情報です。</span><span class="sxs-lookup"><span data-stu-id="07dbd-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07dbd-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="07dbd-115">Return value</span></span>

<span data-ttu-id="07dbd-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="07dbd-116">S_OK</span></span> 
  
> <span data-ttu-id="07dbd-117">フォームが正常に読み込まれました。</span><span class="sxs-lookup"><span data-stu-id="07dbd-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="07dbd-118">備考</span><span class="sxs-lookup"><span data-stu-id="07dbd-118">Remarks</span></span>

<span data-ttu-id="07dbd-119">フォームの閲覧者は、既存のメッセージのフォームをロードする**IPersistMessage::Load**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07dbd-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="07dbd-120">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="07dbd-120">Notes to implementers</span></span>

 <span data-ttu-id="07dbd-121">フォームが状態は、次のいずれかである場合にのみ、**ロード**が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="07dbd-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="07dbd-122">初期化されていません</span><span class="sxs-lookup"><span data-stu-id="07dbd-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="07dbd-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="07dbd-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="07dbd-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="07dbd-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="07dbd-125">フォーム ビューアーは、フォームが他の状態では、**ロード**を呼び出し、メソッドは E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="07dbd-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="07dbd-126">**負荷**に渡される 1 つは別の作業中のメッセージ、サイトへの参照は、フォームに場合、は、使用できなくするために元のサイトをリリースします。</span><span class="sxs-lookup"><span data-stu-id="07dbd-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="07dbd-127">_PMessageSite_と_pMessage_パラメーターからは、サイトのメッセージとメッセージへのポインターを格納し、その参照カウントをインクリメントするのには、両方のオブジェクトの[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07dbd-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="07dbd-128">**AddRef**が完了したら、フォームに、 _ulMessageStatus_と_ulMessageFlags_のパラメーターのプロパティを格納します。</span><span class="sxs-lookup"><span data-stu-id="07dbd-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="07dbd-129">フォームを[通常](normal-state.md)の状態を表示するには、前に移行し、 [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出すことによって登録されている視聴者に通知します。</span><span class="sxs-lookup"><span data-stu-id="07dbd-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="07dbd-130">エラーが発生しない場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="07dbd-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07dbd-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="07dbd-131">See also</span></span>



[<span data-ttu-id="07dbd-132">PidTagMessageFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="07dbd-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="07dbd-133">PidTagMessageStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="07dbd-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="07dbd-134">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="07dbd-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="07dbd-135">初期化されていない状態</span><span class="sxs-lookup"><span data-stu-id="07dbd-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="07dbd-136">HandsOffAfterSave 状態</span><span class="sxs-lookup"><span data-stu-id="07dbd-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="07dbd-137">HandsOffFromNormal 状態</span><span class="sxs-lookup"><span data-stu-id="07dbd-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="07dbd-138">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="07dbd-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="07dbd-139">機能として</span><span class="sxs-lookup"><span data-stu-id="07dbd-139">IPersistStorage::Load</span></span>](http://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="07dbd-140">IPersistStream::Load</span><span class="sxs-lookup"><span data-stu-id="07dbd-140">IPersistStream::Load</span></span>](http://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="07dbd-141">IPersistFile::Load</span><span class="sxs-lookup"><span data-stu-id="07dbd-141">IPersistFile::Load</span></span>](http://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

