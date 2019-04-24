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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282832"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="aaf85-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="aaf85-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="aaf85-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf85-105">保留中の受信または送信メッセージをすべてトランスポートプロバイダーが直ちに配信するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="aaf85-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="aaf85-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aaf85-106">Parameters</span></span>

 <span data-ttu-id="aaf85-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="aaf85-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="aaf85-108">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="aaf85-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="aaf85-109">_cbtargettransport_</span><span class="sxs-lookup"><span data-stu-id="aaf85-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="aaf85-110">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="aaf85-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="aaf85-111">_lptargettransport_</span><span class="sxs-lookup"><span data-stu-id="aaf85-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="aaf85-112">順番予約語NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="aaf85-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="aaf85-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aaf85-113">_ulFlags_</span></span>
  
> <span data-ttu-id="aaf85-114">順番メッセージキューのフラッシュがどのように行われるかを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="aaf85-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="aaf85-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="aaf85-115">The following flags can be set:</span></span>
    
<span data-ttu-id="aaf85-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="aaf85-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="aaf85-117">受信メッセージキューまたはキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aaf85-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="aaf85-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="aaf85-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="aaf85-119">可能であれば、トランスポートプロバイダーはこの要求を処理する必要があります (これを実行すると時間がかかる場合もあります)。</span><span class="sxs-lookup"><span data-stu-id="aaf85-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="aaf85-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="aaf85-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="aaf85-121">トランスポートプロバイダーは、ユーザーインターフェイスを表示しません。</span><span class="sxs-lookup"><span data-stu-id="aaf85-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="aaf85-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="aaf85-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="aaf85-123">送信メッセージキューまたはキューをフラッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aaf85-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aaf85-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="aaf85-124">Return value</span></span>

<span data-ttu-id="aaf85-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="aaf85-125">S_OK</span></span> 
  
> <span data-ttu-id="aaf85-126">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="aaf85-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aaf85-127">解説</span><span class="sxs-lookup"><span data-stu-id="aaf85-127">Remarks</span></span>

<span data-ttu-id="aaf85-128">mapi スプーラーは**IXPLogon:: flushqueues**メソッドを呼び出して、mapi スプーラーがメッセージの処理を開始しようとしていることをトランスポートプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="aaf85-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="aaf85-129">トランスポートプロバイダーは、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを呼び出して、ステータス行の**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティでその状態に適したビットを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aaf85-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="aaf85-130">状態行を更新した後、トランスポートプロバイダーは**flushqueues**呼び出しに対して S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="aaf85-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="aaf85-131">その後、mapi スプーラーは、mapi スプーラーと同期された操作で、メッセージの送信を開始します。</span><span class="sxs-lookup"><span data-stu-id="aaf85-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="aaf85-132">[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドの実装をサポートするために、MAPI スプーラーはプロファイルセッションで実行されているアクティブなトランスポートプロバイダーのすべてのログオンオブジェクトに対して**IXPLogon:: flushqueues**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aaf85-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="aaf85-133">**imapistatus:: flushqueues**へのクライアントアプリケーション呼び出しの結果として、トランスポートプロバイダーの**flushqueues**メソッドが呼び出されると、メッセージ処理はクライアントに非同期で行われます。</span><span class="sxs-lookup"><span data-stu-id="aaf85-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aaf85-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="aaf85-134">See also</span></span>



[<span data-ttu-id="aaf85-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="aaf85-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="aaf85-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aaf85-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

