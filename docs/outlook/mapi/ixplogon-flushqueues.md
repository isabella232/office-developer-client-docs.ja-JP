---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421971"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="0ee68-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="0ee68-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="0ee68-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ee68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ee68-105">トランスポート プロバイダーが保留中のすべての受信メッセージまたは送信メッセージを直ちに配信する要求。</span><span class="sxs-lookup"><span data-stu-id="0ee68-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0ee68-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0ee68-106">Parameters</span></span>

 <span data-ttu-id="0ee68-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0ee68-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0ee68-108">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0ee68-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="0ee68-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="0ee68-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="0ee68-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="0ee68-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="0ee68-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="0ee68-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="0ee68-112">[in]予約済み。NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee68-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="0ee68-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ee68-113">_ulFlags_</span></span>
  
> <span data-ttu-id="0ee68-114">[in]メッセージ キューのフラッシュの実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0ee68-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="0ee68-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0ee68-115">The following flags can be set:</span></span>
    
<span data-ttu-id="0ee68-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="0ee68-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="0ee68-117">受信メッセージ キューまたはキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee68-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="0ee68-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="0ee68-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="0ee68-119">トランスポート プロバイダーは、可能な場合は、時間がかかる場合でも、この要求を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee68-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="0ee68-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="0ee68-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="0ee68-121">トランスポート プロバイダーは、ユーザー インターフェイスを表示しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee68-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="0ee68-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="0ee68-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="0ee68-123">送信メッセージ キューまたはキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee68-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ee68-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="0ee68-124">Return value</span></span>

<span data-ttu-id="0ee68-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ee68-125">S_OK</span></span> 
  
> <span data-ttu-id="0ee68-126">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="0ee68-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ee68-127">注釈</span><span class="sxs-lookup"><span data-stu-id="0ee68-127">Remarks</span></span>

<span data-ttu-id="0ee68-128">MAPI スプーラーは **、IXPLogon::FlushQueues** メソッドを呼び出して、MAPI スプーラーがメッセージの処理を開始する予定であるトランスポート プロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="0ee68-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="0ee68-129">トランスポート プロバイダーは [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出して、状態行の **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの状態に適切なビットを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee68-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="0ee68-130">状態行を更新した後、トランスポート プロバイダーは **FlushQueues** 呼び出しS_OKを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee68-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="0ee68-131">その後、MAPI スプーラーはメッセージの送信を開始し、操作は MAPI スプーラーと同期します。</span><span class="sxs-lookup"><span data-stu-id="0ee68-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="0ee68-132">[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドの実装をサポートするために、MAPI スプーラーは、プロファイル セッションで実行されているアクティブ なトランスポート プロバイダーのすべてのログオン オブジェクトに対して **IXPLogon::FlushQueues** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0ee68-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="0ee68-133">**IMAPIStatus::FlushQueues** へのクライアント アプリケーション呼び出しの結果としてトランスポート プロバイダーの **FlushQueues** メソッドが呼び出された場合、メッセージ処理はクライアントに対して非同期的に行われます。</span><span class="sxs-lookup"><span data-stu-id="0ee68-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ee68-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ee68-134">See also</span></span>



[<span data-ttu-id="0ee68-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="0ee68-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="0ee68-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ee68-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

