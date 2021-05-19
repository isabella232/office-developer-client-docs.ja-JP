---
title: IMAPIStatusFlushQueues
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
# <a name="imapistatusflushqueues"></a><span data-ttu-id="4cb4f-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="4cb4f-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="4cb4f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cb4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cb4f-105">送信または受信を待機しているすべてのメッセージを、すぐにアップロードまたはダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="4cb4f-106">トランスポート プロバイダーが実装する MAPI スプーラー状態オブジェクトと状態オブジェクトは、このメソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4cb4f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4cb4f-107">Parameters</span></span>

 <span data-ttu-id="4cb4f-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4cb4f-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="4cb4f-109">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="4cb4f-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="4cb4f-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="4cb4f-111">[in]  _lpTargetTransport_ パラメーターが指すエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="4cb4f-112">_cbTargetTransport_ パラメーターは、MAPI スプーラーの状態オブジェクトへの呼び出しでのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="4cb4f-113">トランスポート プロバイダーへの呼び出しの場合  _、cbTargetTransport_ パラメーターは 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="4cb4f-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="4cb4f-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="4cb4f-115">[in]メッセージ キューをフラッシュするトランスポート プロバイダーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="4cb4f-116">_lpTargetTransport パラメーター_ は、MAPI スプーラーの状態オブジェクトの呼び出しでのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="4cb4f-117">トランスポート プロバイダーへの呼び出しの場合  _、lpTargetTransport_ パラメーターは NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="4cb4f-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4cb4f-118">_ulFlags_</span></span>
  
> <span data-ttu-id="4cb4f-119">[in]フラッシュ操作を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="4cb4f-120">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-120">The following flags can be set:</span></span>
    
<span data-ttu-id="4cb4f-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="4cb4f-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="4cb4f-122">フラッシュ操作は非同期的に行われます。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="4cb4f-123">このフラグは、MAPI スプーラーの状態オブジェクトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="4cb4f-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="4cb4f-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="4cb4f-125">受信メッセージ キューはフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="4cb4f-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="4cb4f-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="4cb4f-127">フラッシュ操作は、パフォーマンスが低下する可能性があるにもかかわらず、関係なく発生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="4cb4f-128">このフラグは、非同期トランスポート プロバイダーを対象とする場合に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="4cb4f-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="4cb4f-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="4cb4f-130">status オブジェクトは進行状況インジケーターを表示しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="4cb4f-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="4cb4f-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="4cb4f-132">送信メッセージ キューはフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4cb4f-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="4cb4f-133">Return value</span></span>

<span data-ttu-id="4cb4f-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="4cb4f-134">S_OK</span></span> 
  
> <span data-ttu-id="4cb4f-135">フラッシュ操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="4cb4f-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="4cb4f-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="4cb4f-137">別の操作が進行中です。この操作を開始する前に、完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="4cb4f-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4cb4f-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4cb4f-139">status オブジェクトは、status オブジェクトの PR_RESOURCE_METHODS **(** [PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_FLUSH_QUEUES フラグがない場合に示されるこの操作をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4cb4f-140">注釈</span><span class="sxs-lookup"><span data-stu-id="4cb4f-140">Remarks</span></span>

<span data-ttu-id="4cb4f-141">**IMAPIStatus::FlushQueues** メソッドは、MAPI スプーラーまたはトランスポート プロバイダーが送信キュー内のすべてのメッセージを直ちに送信するか、受信キューからすべてのメッセージを受信する要求を行います。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="4cb4f-142">**FlushQueues は** 、MAPI スプーラーの状態オブジェクトとトランスポート プロバイダーが提供する状態オブジェクトによってのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="4cb4f-143">MAPI_E_BUSYを続行できるよう、非同期要求に対して返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="4cb4f-144">既定では **、FlushQueues は** 同期操作です。フラッシュが完了するまで、コントロールは呼び出し元に戻しません。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="4cb4f-145">MAPI スプーラーによって実行されるフラッシュ操作のみを非同期にできます。クライアントは、この動作を要求するには、FLUSH_ASYNC_OKフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4cb4f-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="4cb4f-146">Notes to implementers</span></span>

<span data-ttu-id="4cb4f-147">リモート トランスポート プロバイダーによる **FlushQueues** の実装では、ログオン オブジェクトの状態行の **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティのビットを設定して、キューのフラッシュ方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="4cb4f-148">リモート ビューアーが FLUSH_UPLOAD フラグを渡す場合 **、FlushQueues** メソッドは、STATUS_INBOUND_ENABLEDビットとSTATUS_INBOUND_ACTIVEする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="4cb4f-149">リモート ビューアーが FLUSH_DOWNLOAD フラグを渡す場合 **、FlushQueues** メソッドは、STATUS_OUTBOUND_ENABLEDビットSTATUS_OUTBOUND_ACTIVEする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="4cb4f-150">**FlushQueues は、** 次にデータをS_OK。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="4cb4f-151">MAPI スプーラーは、メッセージをアップロードおよびダウンロードするための適切なアクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4cb4f-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4cb4f-152">Notes to callers</span></span>

<span data-ttu-id="4cb4f-153">MAPI スプーラー状態オブジェクトへの呼び出しは、すべてのメッセージを適切なトランスポート プロバイダーと転送するディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="4cb4f-154">個々のトランスポート プロバイダーの状態オブジェクトを呼び出す場合、そのプロバイダーのメッセージだけが影響を受ける。</span><span class="sxs-lookup"><span data-stu-id="4cb4f-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4cb4f-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cb4f-155">See also</span></span>



[<span data-ttu-id="4cb4f-156">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4cb4f-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="4cb4f-157">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4cb4f-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="4cb4f-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4cb4f-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

