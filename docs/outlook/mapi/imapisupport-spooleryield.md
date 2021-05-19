---
title: IMAPISupportSpoolerYield
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409910"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="982a8-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="982a8-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="982a8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="982a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="982a8-105">MAPI スプーラーに CPU を制御し、必要と見なされるタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="982a8-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="982a8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="982a8-106">Parameters</span></span>

 <span data-ttu-id="982a8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="982a8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="982a8-108">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="982a8-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="982a8-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="982a8-109">Return value</span></span>

<span data-ttu-id="982a8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="982a8-110">S_OK</span></span> 
  
> <span data-ttu-id="982a8-111">トランスポート プロバイダーが CPU を正常にリリースしました。</span><span class="sxs-lookup"><span data-stu-id="982a8-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="982a8-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="982a8-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="982a8-113">まだ受信していない受信者へのメッセージの配信を停止するようにトランスポート プロバイダーに指示します。</span><span class="sxs-lookup"><span data-stu-id="982a8-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="982a8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="982a8-114">Remarks</span></span>

<span data-ttu-id="982a8-115">**IMAPISupport::SpoolerYield** メソッドは、トランスポート プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="982a8-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="982a8-116">トランスポート プロバイダーは **、MAPI スプーラーが** 必要な処理を実行するためにスプーラーYield を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="982a8-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="982a8-117">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="982a8-117">Notes to callers</span></span>

<span data-ttu-id="982a8-118">一 **時停止できる長い** 操作を実行する場合は、SpoolerYield を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="982a8-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="982a8-119">これにより、ビジー 状態のネットワーク上の大規模な受信者リストへの配信など、長時間の操作中にフォアグラウンド アプリケーションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="982a8-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="982a8-120">**SpoolerYield** がメッセージをMAPI_W_CANCEL_MESSAGE場合、MAPI スプーラーはメッセージを送信しなくなると判断しました。</span><span class="sxs-lookup"><span data-stu-id="982a8-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="982a8-121">可能MAPI_E_USER_CANCEL呼び出し元のプロセスに戻り、終了します。</span><span class="sxs-lookup"><span data-stu-id="982a8-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="982a8-122">MAPI スプーラーに対する処理の詳細については、「MAPI スプーラーとの対話 [」を参照してください](interacting-with-the-mapi-spooler.md)。</span><span class="sxs-lookup"><span data-stu-id="982a8-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="982a8-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="982a8-123">See also</span></span>



[<span data-ttu-id="982a8-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="982a8-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

