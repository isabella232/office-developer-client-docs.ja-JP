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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329039"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="ee1a2-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="ee1a2-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="ee1a2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee1a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee1a2-105">MAPI スプーラーに CPU を制御します。これにより、必要なタスクを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ee1a2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ee1a2-106">Parameters</span></span>

 <span data-ttu-id="ee1a2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee1a2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ee1a2-108">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee1a2-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="ee1a2-109">Return value</span></span>

<span data-ttu-id="ee1a2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee1a2-110">S_OK</span></span> 
  
> <span data-ttu-id="ee1a2-111">トランスポートプロバイダーが CPU を正常に解放しました。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="ee1a2-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="ee1a2-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="ee1a2-113">トランスポートプロバイダーに対して、まだ受信していない受信者に対するメッセージの配信を停止するように指示します。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee1a2-114">解説</span><span class="sxs-lookup"><span data-stu-id="ee1a2-114">Remarks</span></span>

<span data-ttu-id="ee1a2-115">**imapisupport:: SpoolerYield**メソッドは、トランスポートプロバイダーのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="ee1a2-116">トランスポートプロバイダーは、 **SpoolerYield**を呼び出して、MAPI スプーラーで必要な処理を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee1a2-117">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ee1a2-117">Notes to callers</span></span>

<span data-ttu-id="ee1a2-118">一時停止できる長時間の操作を実行している場合は、 **SpoolerYield**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="ee1a2-119">これにより、混雑したネットワークを介して大きな受信者リストへの配信など、長時間の操作中にフォアグラウンドアプリケーションが実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="ee1a2-120">**SpoolerYield**が MAPI_W_CANCEL_MESSAGE を返した場合、MAPI スプーラーはメッセージを送信する必要がないと判断しました。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="ee1a2-121">MAPI_E_USER_CANCEL を呼び出しプロセスに返し、可能であれば終了します。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="ee1a2-122">mapi スプーラーへの追加の詳細については、「 [mapi スプーラーとの対話](interacting-with-the-mapi-spooler.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee1a2-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee1a2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee1a2-123">See also</span></span>



[<span data-ttu-id="ee1a2-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee1a2-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

