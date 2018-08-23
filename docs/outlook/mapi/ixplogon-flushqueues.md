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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 961ac2d26cd58e625c35d00bd1216cdee2ce57a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584731"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="1b526-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1b526-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="1b526-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b526-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b526-105">要求がトランスポート プロバイダーは、すべての保留の受信または送信メッセージを即座に配信します。</span><span class="sxs-lookup"><span data-stu-id="1b526-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1b526-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1b526-106">Parameters</span></span>

 <span data-ttu-id="1b526-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1b526-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1b526-108">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="1b526-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="1b526-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="1b526-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="1b526-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="1b526-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1b526-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="1b526-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="1b526-112">[in]予約されています。NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b526-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="1b526-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b526-113">_ulFlags_</span></span>
  
> <span data-ttu-id="1b526-114">[in]メッセージ キューのフラッシュを実現する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="1b526-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="1b526-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1b526-115">The following flags can be set:</span></span>
    
<span data-ttu-id="1b526-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1b526-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1b526-117">受信メッセージのキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b526-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="1b526-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="1b526-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="1b526-119">トランスポート プロバイダーは、これは時間がかかる場合でもこの要求を可能であれば、処理されます。</span><span class="sxs-lookup"><span data-stu-id="1b526-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="1b526-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="1b526-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="1b526-121">トランスポート プロバイダーは、ユーザー インターフェイスを表示しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b526-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="1b526-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="1b526-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="1b526-123">送信メッセージのキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b526-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1b526-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1b526-124">Return value</span></span>

<span data-ttu-id="1b526-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b526-125">S_OK</span></span> 
  
> <span data-ttu-id="1b526-126">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="1b526-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b526-127">注釈</span><span class="sxs-lookup"><span data-stu-id="1b526-127">Remarks</span></span>

<span data-ttu-id="1b526-128">MAPI スプーラーは、MAPI スプーラーがメッセージの処理を開始しようとしていますが、トランスポート プロバイダーに通知する**IXPLogon::FlushQueues**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1b526-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="1b526-129">トランスポート プロバイダーは、 **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティの [状態] 行で、適切なビットの状態を設定するのには[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b526-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="1b526-130">その [状態] 行を更新した後には、トランスポート プロバイダーは、必要があります、 **FlushQueues**の呼び出しに、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="1b526-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="1b526-131">MAPI スプーラーは、MAPI スプーラーを無効に同期されている操作をメッセージの送信を開始します。</span><span class="sxs-lookup"><span data-stu-id="1b526-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="1b526-132">[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドの実装をサポートするためには、MAPI スプーラーは、ログオン オブジェクトのすべてのプロファイル セッションで実行されているアクティブなトランスポート プロバイダーの**IXPLogon::FlushQueues**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1b526-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="1b526-133">**IMAPIStatus::FlushQueues**クライアント アプリケーションの呼び出しによって、トランスポート プロバイダーの**FlushQueues**メソッドを呼び出すと、クライアントにメッセージの処理が非同期に発生します。</span><span class="sxs-lookup"><span data-stu-id="1b526-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b526-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b526-134">See also</span></span>



[<span data-ttu-id="1b526-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1b526-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="1b526-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b526-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

