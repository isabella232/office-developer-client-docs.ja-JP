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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317130"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="49083-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="49083-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="49083-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49083-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49083-105">指定したメッセージのフォームを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="49083-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="49083-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49083-106">Parameters</span></span>

 <span data-ttu-id="49083-107">_pメッセージ ite_</span><span class="sxs-lookup"><span data-stu-id="49083-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="49083-108">順番フォームを読み込むためのメッセージサイトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="49083-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="49083-109">_pmessage_</span><span class="sxs-lookup"><span data-stu-id="49083-109">_pMessage_</span></span>
  
> <span data-ttu-id="49083-110">順番フォームを読み込むメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="49083-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="49083-111">_ulmessagestatus_</span><span class="sxs-lookup"><span data-stu-id="49083-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="49083-112">順番メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーし、メッセージの状態に関する情報を提供する、クライアント定義またはプロバイダー定義のフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="49083-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="49083-113">_ulmessageflags_</span><span class="sxs-lookup"><span data-stu-id="49083-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="49083-114">順番メッセージの状態に関する詳細情報を提供するフラグのビットマスク。メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="49083-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="49083-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="49083-115">Return value</span></span>

<span data-ttu-id="49083-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="49083-116">S_OK</span></span> 
  
> <span data-ttu-id="49083-117">フォームが正常に読み込まれました。</span><span class="sxs-lookup"><span data-stu-id="49083-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49083-118">解説</span><span class="sxs-lookup"><span data-stu-id="49083-118">Remarks</span></span>

<span data-ttu-id="49083-119">フォームビューアーは**IPersistMessage:: load**メソッドを呼び出して、既存のメッセージのフォームを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="49083-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="49083-120">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="49083-120">Notes to implementers</span></span>

 <span data-ttu-id="49083-121">**Load**は、フォームが次のいずれかの状態にある場合にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="49083-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="49083-122">初期化されていません</span><span class="sxs-lookup"><span data-stu-id="49083-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="49083-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="49083-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="49083-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="49083-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="49083-125">フォームが他の状態にあるときにフォームビューアーが**Load**を呼び出すと、メソッドは E_UNEXPECTED を返します。</span><span class="sxs-lookup"><span data-stu-id="49083-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="49083-126">フォームに、**読み込み**に渡されたものとは異なるアクティブなメッセージサイトへの参照がある場合は、そのサイトが使用されなくなったため、元のサイトを解放します。</span><span class="sxs-lookup"><span data-stu-id="49083-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="49083-127">メッセージサイトおよびメッセージへのポインターを pメッセージパラメーター __ と_pmessage_パラメーターから格納し、両方のオブジェクト ' [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して参照カウントをインクリメントします。</span><span class="sxs-lookup"><span data-stu-id="49083-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="49083-128">**AddRef**が完了したら、 _ulmessagestatus_パラメーターと_ulmessagestatus_パラメーターのプロパティをフォームに格納します。</span><span class="sxs-lookup"><span data-stu-id="49083-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="49083-129">フォームを表示する前に[通常](normal-state.md)の状態に移行し、 [IMAPIViewAdviseSink:: onnewmessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出して、登録されているビューアーに通知します。</span><span class="sxs-lookup"><span data-stu-id="49083-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="49083-130">エラーが発生しない場合は、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="49083-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49083-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="49083-131">See also</span></span>



[<span data-ttu-id="49083-132">PidTagMessageFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49083-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="49083-133">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="49083-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="49083-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49083-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="49083-135">未初期化状態</span><span class="sxs-lookup"><span data-stu-id="49083-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="49083-136">保存の状態を処理する</span><span class="sxs-lookup"><span data-stu-id="49083-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="49083-137">標準の状態</span><span class="sxs-lookup"><span data-stu-id="49083-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="49083-138">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="49083-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="49083-139">IPersistStorage:: Load</span><span class="sxs-lookup"><span data-stu-id="49083-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="49083-140">IPersistStream:: Load</span><span class="sxs-lookup"><span data-stu-id="49083-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="49083-141">IPersistFile:: Load</span><span class="sxs-lookup"><span data-stu-id="49083-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

