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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d6c221ae307edb9d84cfcc0026660ea4bce7fadd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800713"
---
# <a name="imapistatusflushqueues"></a><span data-ttu-id="ed095-103">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="ed095-103">IMAPIStatus::FlushQueues</span></span>

  
  
<span data-ttu-id="ed095-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed095-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed095-105">送信またはアップロードまたはダウンロードをすぐに受信を待機しているすべてのメッセージを強制的にします。</span><span class="sxs-lookup"><span data-stu-id="ed095-105">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span> <span data-ttu-id="ed095-106">MAPI スプーラーの状態のオブジェクトおよびトランスポート プロバイダーを実装する状態オブジェクトは、このメソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed095-106">The MAPI spooler status object and status objects that transport providers implement support this method.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ed095-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ed095-107">Parameters</span></span>

 <span data-ttu-id="ed095-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ed095-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="ed095-109">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="ed095-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="ed095-110">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="ed095-110">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="ed095-111">[in]_LpTargetTransport_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="ed095-111">[in] The byte count in the entry identifier pointed to by the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="ed095-112">_CbTargetTransport_パラメーターは、MAPI スプーラーを無効の状態のオブジェクトへの呼び出しでのみ設定されています。</span><span class="sxs-lookup"><span data-stu-id="ed095-112">The  _cbTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="ed095-113">トランスポート プロバイダーへの呼び出し、 _cbTargetTransport_パラメーターが 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ed095-113">For calls to a transport provider, the  _cbTargetTransport_ parameter is set to 0.</span></span> 
    
 <span data-ttu-id="ed095-114">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="ed095-114">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="ed095-115">[in]そのメッセージ キューをフラッシュするのには、トランスポート プロバイダーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ed095-115">[in] A pointer to the entry identifier of the transport provider that is to flush its message queues.</span></span> <span data-ttu-id="ed095-116">_LpTargetTransport_パラメーターは、MAPI スプーラーを無効の状態のオブジェクトへの呼び出しでのみ設定されています。</span><span class="sxs-lookup"><span data-stu-id="ed095-116">The  _lpTargetTransport_ parameter is set only on calls to the MAPI spooler's status object.</span></span> <span data-ttu-id="ed095-117">トランスポート プロバイダーへの呼び出し、 _lpTargetTransport_パラメーターは NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="ed095-117">For calls to a transport provider, the  _lpTargetTransport_ parameter is set to NULL.</span></span> 
    
 <span data-ttu-id="ed095-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ed095-118">_ulFlags_</span></span>
  
> <span data-ttu-id="ed095-119">[in]フラッシュ操作を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ed095-119">[in] A bitmask of flags that controls the flush operation.</span></span> <span data-ttu-id="ed095-120">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ed095-120">The following flags can be set:</span></span>
    
<span data-ttu-id="ed095-121">FLUSH_ASYNC_OK</span><span class="sxs-lookup"><span data-stu-id="ed095-121">FLUSH_ASYNC_OK</span></span> 
  
> <span data-ttu-id="ed095-122">フラッシュ操作が非同期的に発生することができます。</span><span class="sxs-lookup"><span data-stu-id="ed095-122">The flush operation can occur asynchronously.</span></span> <span data-ttu-id="ed095-123">このフラグは、MAPI スプーラーを無効の状態のオブジェクトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ed095-123">This flag applies only to the MAPI spooler's status object.</span></span> 
    
<span data-ttu-id="ed095-124">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ed095-124">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="ed095-125">受信メッセージ キューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed095-125">The incoming message queues should be flushed.</span></span>
    
<span data-ttu-id="ed095-126">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="ed095-126">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="ed095-127">フラッシュ操作にする必要がありますパフォーマンスが低下する可能性も関係なく、発生します。</span><span class="sxs-lookup"><span data-stu-id="ed095-127">The flush operation should occur regardless, in spite of the chance of a decrease in performance.</span></span> <span data-ttu-id="ed095-128">非同期型のトランスポート プロバイダーを対象としたとき、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed095-128">This flag must be set when an asynchronous transport provider is targeted.</span></span>
    
<span data-ttu-id="ed095-129">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="ed095-129">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="ed095-130">ステータス オブジェクトでは、進行状況のインジケーターが表示されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed095-130">The status object should not display a progress indicator.</span></span>
    
<span data-ttu-id="ed095-131">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="ed095-131">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="ed095-132">送信メッセージのキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed095-132">The outgoing message queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ed095-133">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ed095-133">Return value</span></span>

<span data-ttu-id="ed095-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed095-134">S_OK</span></span> 
  
> <span data-ttu-id="ed095-135">フラッシュ操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="ed095-135">The flush operation was successful.</span></span>
    
<span data-ttu-id="ed095-136">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ed095-136">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ed095-137">別の操作が実行中です。完了するために許可するか、停止する、この操作を開始する前に。</span><span class="sxs-lookup"><span data-stu-id="ed095-137">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation can be initiated.</span></span>
    
<span data-ttu-id="ed095-138">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ed095-138">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ed095-139">状態オブジェクトは、この操作をサポートしていません状態オブジェクトの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティに STATUS_FLUSH_QUEUES フラグがない場合で示される。</span><span class="sxs-lookup"><span data-stu-id="ed095-139">The status object does not support this operation, as indicated by the absence of the STATUS_FLUSH_QUEUES flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed095-140">注釈</span><span class="sxs-lookup"><span data-stu-id="ed095-140">Remarks</span></span>

<span data-ttu-id="ed095-141">**IMAPIStatus::FlushQueues**メソッドは、MAPI スプーラーを無効またはトランスポート プロバイダーすぐに発信キュー内のすべてのメッセージを送信または受信キューからすべてのメッセージを受信するを要求します。</span><span class="sxs-lookup"><span data-stu-id="ed095-141">The **IMAPIStatus::FlushQueues** method requests that the MAPI spooler or a transport provider immediately send all messages in the outgoing queue or receive all messages from the incoming queue.</span></span> <span data-ttu-id="ed095-142">**FlushQueues**は、MAPI スプーラーの状態のオブジェクトのみが、トランスポート プロバイダーの供給状態のオブジェクトによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ed095-142">**FlushQueues** is implemented only by the MAPI spooler status object and by status objects that transport providers supply.</span></span> 
  
<span data-ttu-id="ed095-143">非同期要求のクライアントは、作業を続行できるように、MAPI_E_BUSY が返されます。</span><span class="sxs-lookup"><span data-stu-id="ed095-143">MAPI_E_BUSY should be returned for asynchronous requests so that clients can continue work.</span></span> 
  
<span data-ttu-id="ed095-144">既定では、 **FlushQueues**は、同期操作です。フラッシュが完了するまで、制御は呼び出し側に返されません。</span><span class="sxs-lookup"><span data-stu-id="ed095-144">By default, **FlushQueues** is a synchronous operation; control does not return to the caller until the flush has completed.</span></span> <span data-ttu-id="ed095-145">のみ、フラッシュ操作 MAPI スプーラーが実行できる可能性があります。クライアントは、FLUSH_ASYNC_OK フラグを設定することによってこの動作を要求します。</span><span class="sxs-lookup"><span data-stu-id="ed095-145">Only the flush operation performed by the MAPI spooler can be asynchronous; clients request this behavior by setting the FLUSH_ASYNC_OK flag.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ed095-146">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="ed095-146">Notes to implementers</span></span>

<span data-ttu-id="ed095-147">**FlushQueues**のリモート トランスポート プロバイダーの実装では、キューをフラッシュする方法を制御するため、ログオン オブジェクトの [状態] 行で、 **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティのビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="ed095-147">A remote transport provider's implementation of **FlushQueues** sets bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property in the logon object's status row to control how queues are flushed.</span></span> <span data-ttu-id="ed095-148">リモート ビューアーは、FLUSH_UPLOAD フラグに合格した場合、 **FlushQueues**メソッドは、STATUS_INBOUND_ENABLED と STATUS_INBOUND_ACTIVE のビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="ed095-148">If a remote viewer passes in the FLUSH_UPLOAD flag, the **FlushQueues** method should set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits.</span></span> <span data-ttu-id="ed095-149">リモート ビューアーは、FLUSH_DOWNLOAD フラグに合格した場合、 **FlushQueues**メソッドは、STATUS_OUTBOUND_ENABLED と STATUS_OUTBOUND_ACTIVE のビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="ed095-149">If a remote viewer passes in the FLUSH_DOWNLOAD flag, the **FlushQueues** method should set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits.</span></span> <span data-ttu-id="ed095-150">**FlushQueues**では、S_OK を返す必要がありますし。</span><span class="sxs-lookup"><span data-stu-id="ed095-150">**FlushQueues** should then return S_OK.</span></span> <span data-ttu-id="ed095-151">MAPI スプーラーを無効にし、アップロードし、メッセージをダウンロードするには、適切なアクションが開始されます。</span><span class="sxs-lookup"><span data-stu-id="ed095-151">The MAPI spooler will then initiate the appropriate actions to upload and download messages.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ed095-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ed095-152">Notes to callers</span></span>

<span data-ttu-id="ed095-153">MAPI スプーラーの状態のオブジェクトへの呼び出しは、するか、適切なトランスポート プロバイダーからすべてのメッセージを転送するディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="ed095-153">A call to the MAPI spooler status object is a directive to transfer all messages either to or from the appropriate transport provider.</span></span> <span data-ttu-id="ed095-154">個々 のトランスポート プロバイダーの状態のオブジェクトを呼び出すと、そのプロバイダーのメッセージだけが影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="ed095-154">When you call an individual transport provider's status object, only the messages for that provider are affected.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed095-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed095-155">See also</span></span>



[<span data-ttu-id="ed095-156">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed095-156">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="ed095-157">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed095-157">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
  
[<span data-ttu-id="ed095-158">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ed095-158">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

