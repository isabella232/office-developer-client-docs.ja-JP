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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6e917991e109ac04a14ea7d93eebcf9cce835845
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800794"
---
# <a name="imapisupportspooleryield"></a><span data-ttu-id="18721-103">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="18721-103">IMAPISupport::SpoolerYield</span></span>

  
  
<span data-ttu-id="18721-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18721-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18721-105">必要と見なされるすべてのタスクを実行できるように、MAPI スプーラーを CPU の制御を提供します。</span><span class="sxs-lookup"><span data-stu-id="18721-105">Gives control of the CPU to the MAPI spooler so that it can perform any tasks it considers necessary.</span></span>
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="18721-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="18721-106">Parameters</span></span>

 <span data-ttu-id="18721-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="18721-107">_ulFlags_</span></span>
  
> <span data-ttu-id="18721-108">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="18721-108">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="18721-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="18721-109">Return value</span></span>

<span data-ttu-id="18721-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="18721-110">S_OK</span></span> 
  
> <span data-ttu-id="18721-111">トランスポート プロバイダーでは、CPU が解放されました。</span><span class="sxs-lookup"><span data-stu-id="18721-111">The transport provider successfully released the CPU.</span></span>
    
<span data-ttu-id="18721-112">MAPI_W_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="18721-112">MAPI_W_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="18721-113">トランスポート プロバイダーをまだ受け取っていないことを受信者にメッセージの配信を停止するように指示します。</span><span class="sxs-lookup"><span data-stu-id="18721-113">Instructs the transport provider to stop the delivery of the message to any recipients that have not yet received it.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18721-114">備考</span><span class="sxs-lookup"><span data-stu-id="18721-114">Remarks</span></span>

<span data-ttu-id="18721-115">トランスポート プロバイダーのサポート オブジェクトの**IMAPISupport::SpoolerYield**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="18721-115">The **IMAPISupport::SpoolerYield** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="18721-116">トランスポート プロバイダーは、必要な処理を実行するのには MAPI スプーラーを許可するのには**SpoolerYield**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="18721-116">Transport providers call **SpoolerYield** to allow the MAPI spooler to accomplish any necessary processing.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="18721-117">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="18721-117">Notes to callers</span></span>

<span data-ttu-id="18721-118">一時停止することができますが、時間のかかる操作を実行している場合は、 **SpoolerYield**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="18721-118">Call **SpoolerYield** when you are performing lengthy operations that can be paused.</span></span> <span data-ttu-id="18721-119">これにより、フォア グラウンド アプリケーションがビジー状態のネットワークの間で大きな受信者リストへの配信など、長時間のオペレーション中に実行できます。</span><span class="sxs-lookup"><span data-stu-id="18721-119">This allows foreground applications to run during a long operation, such as delivery to a large recipient list across a busy network.</span></span> 
  
<span data-ttu-id="18721-120">**SpoolerYield**は、MAPI_W_CANCEL_MESSAGE で返された場合、メッセージを送信できなくする必要があります、MAPI スプーラーを無効と判断しました。</span><span class="sxs-lookup"><span data-stu-id="18721-120">If **SpoolerYield** returns with MAPI_W_CANCEL_MESSAGE, the MAPI spooler has determined that the message should no longer be sent.</span></span> <span data-ttu-id="18721-121">可能な場合は、呼び出し元のプロセスと終了時に MAPI_E_USER_CANCEL を返します。</span><span class="sxs-lookup"><span data-stu-id="18721-121">Return MAPI_E_USER_CANCEL to your calling process and exit, if possible.</span></span> 
  
<span data-ttu-id="18721-122">MAPI スプーラーを生成の詳細については、 [MAPI スプーラーと対話する](interacting-with-the-mapi-spooler.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18721-122">For more information about yielding to the MAPI spooler, see [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18721-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="18721-123">See also</span></span>



[<span data-ttu-id="18721-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="18721-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

