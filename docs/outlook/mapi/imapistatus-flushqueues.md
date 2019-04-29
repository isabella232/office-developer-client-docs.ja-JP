---
title: imapistatusflushqueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432605"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="079de-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="079de-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="079de-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="079de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="079de-105">送信または受信を待機しているすべてのメッセージを直ちにアップロードまたはダウンロードすることを強制します。</span><span class="sxs-lookup"><span data-stu-id="079de-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="079de-106">トランスポートプロバイダーが実装する MAPI スプーラー状態オブジェクトと状態オブジェクトは、このメソッドをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="079de-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="079de-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="079de-107">Parameters</span></span>

 <span data-ttu-id="079de-108">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="079de-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="079de-109">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="079de-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="079de-110">_cbtargettransport_</span><span class="sxs-lookup"><span data-stu-id="079de-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="079de-111">順番_lptargettransport_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="079de-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="079de-112">_cbtargettransport_パラメーターは、MAPI スプーラーの status オブジェクトへの呼び出しに対してのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="079de-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="079de-113">トランスポートプロバイダーの呼び出しの場合、 _cbtargettransport_パラメーターは0に設定されます。</span><span class="sxs-lookup"><span data-stu-id="079de-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="079de-114">_lptargettransport_</span><span class="sxs-lookup"><span data-stu-id="079de-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="079de-115">順番メッセージキューをフラッシュするトランスポートプロバイダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="079de-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="079de-116">_lptargettransport_パラメーターは、MAPI スプーラーの status オブジェクトへの呼び出しに対してのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="079de-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="079de-117">トランスポートプロバイダーの呼び出しの場合、 _lptargettransport_パラメーターは NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="079de-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="079de-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="079de-118">_ulFlags_</span></span>
  
> <span data-ttu-id="079de-119">順番フラッシュ操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="079de-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="079de-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="079de-120">The following flags can be set:</span></span>
    
<span data-ttu-id="079de-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="079de-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="079de-122">フラッシュ操作は非同期的に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="079de-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="079de-123">このフラグは、MAPI スプーラーの状態オブジェクトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="079de-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="079de-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="079de-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="079de-125">受信メッセージキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="079de-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="079de-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="079de-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="079de-127">フラッシュ操作は、パフォーマンスが低下する可能性があるにもかかわらず、発生します。</span><span class="sxs-lookup"><span data-stu-id="079de-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="079de-128">このフラグは、非同期トランスポートプロバイダーを対象とする場合に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="079de-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="079de-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="079de-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="079de-130">status オブジェクトは、進行状況インジケーターを表示しません。</span><span class="sxs-lookup"><span data-stu-id="079de-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="079de-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="079de-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="079de-132">送信メッセージキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="079de-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="079de-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="079de-133">Return value</span></span>

<span data-ttu-id="079de-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="079de-134">S_OK</span></span> 
  
> <span data-ttu-id="079de-135">フラッシュ操作が正常に終了しました。</span><span class="sxs-lookup"><span data-stu-id="079de-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="079de-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="079de-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="079de-137">別の操作が進行中です。この操作を開始するには、これを完了させるか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="079de-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="079de-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="079de-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="079de-139">status オブジェクトの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_FLUSH_QUEUES フラグが設定されていない場合、status オブジェクトはこの操作をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="079de-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="079de-140">注釈</span><span class="sxs-lookup"><span data-stu-id="079de-140">Remarks</span></span>

<span data-ttu-id="079de-141">**imapistatus:: flushqueues**メソッドは、MAPI スプーラーまたはトランスポートプロバイダーが、送信キュー内のすべてのメッセージを直ちに送信するか、または受信キューからすべてのメッセージを受信することを要求します。</span><span class="sxs-lookup"><span data-stu-id="079de-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="079de-142">**flushqueues**は、トランスポートプロバイダーが提供する MAPI スプーラー状態オブジェクトと状態オブジェクトによってのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="079de-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="079de-143">クライアントが処理を続行できるように、非同期要求に対して MAPI_E_BUSY を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="079de-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="079de-144">既定では、 **flushqueues**は同期操作です。コントロールは、フラッシュが完了するまで呼び出し元に戻りません。</span><span class="sxs-lookup"><span data-stu-id="079de-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="079de-145">MAPI スプーラーによって実行されるフラッシュ操作だけが非同期になることができます。クライアントは、FLUSH_ASYNC_OK フラグを設定してこの動作を要求します。</span><span class="sxs-lookup"><span data-stu-id="079de-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="079de-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="079de-146">Notes to implementers</span></span>

<span data-ttu-id="079de-147">リモートトランスポートプロバイダーの**flushqueues**の実装は、キューのフラッシュ方法を制御するために、ログオンオブジェクトの状態行の**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティにビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="079de-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="079de-148">リモートビューアーが FLUSH_UPLOAD フラグを渡す場合、 **flushqueues**メソッドは STATUS_INBOUND_ENABLED と STATUS_INBOUND_ACTIVE ビットを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="079de-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="079de-149">リモートビューアーが FLUSH_DOWNLOAD フラグを渡す場合、 **flushqueues**メソッドは STATUS_OUTBOUND_ENABLED と STATUS_OUTBOUND_ACTIVE ビットを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="079de-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="079de-150">**flushqueues**は S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="079de-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="079de-151">その後、MAPI スプーラーは、メッセージをアップロードしてダウンロードするための適切なアクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="079de-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="079de-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="079de-152">Notes to callers</span></span>

<span data-ttu-id="079de-153">MAPI スプーラー状態オブジェクトの呼び出しは、適切なトランスポートプロバイダーとの間のすべてのメッセージを転送するためのディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="079de-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="079de-154">個別のトランスポートプロバイダーの status オブジェクトを呼び出すと、そのプロバイダーのメッセージのみが影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="079de-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="079de-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="079de-155">See also</span></span>



[<span data-ttu-id="079de-156">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="079de-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="079de-157">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="079de-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="079de-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="079de-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

