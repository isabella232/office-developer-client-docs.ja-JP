---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 447832d88a9740875fcf39a32adcf4ebb99e05ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800444"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="b27f1-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="b27f1-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="b27f1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b27f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b27f1-105">MAPI クライアントのクライアントのプロセスを即座に終了するという意図を示しています。</span><span class="sxs-lookup"><span data-stu-id="b27f1-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="b27f1-106">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b27f1-106">Return value</span></span>

<span data-ttu-id="b27f1-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="b27f1-107">S_OK</span></span>
  
> <span data-ttu-id="b27f1-108">MAPI クライアントは、すぐに終了して、MAPI プロバイダーは、クライアントの終了の準備ができて読み込まれている MAPI プロバイダーに、MAPI サブシステムを示しています。</span><span class="sxs-lookup"><span data-stu-id="b27f1-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="b27f1-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b27f1-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="b27f1-110">MAPI サブシステムは、クライアントの高速シャット ダウンをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b27f1-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b27f1-111">備考</span><span class="sxs-lookup"><span data-stu-id="b27f1-111">Remarks</span></span>

<span data-ttu-id="b27f1-112">MAPI クライアントの高速シャット ダウンからのデータの損失を避けるためには、MAPI クライアントが、MAPI サブシステムによって返される S_OK の結果に基づく[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)と**IMAPIClientShutdown::DoFastShutdown**のメソッドを呼び出す必要があります。[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="b27f1-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="b27f1-113">詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b27f1-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b27f1-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="b27f1-114">See also</span></span>



[<span data-ttu-id="b27f1-115">IMAPIClientShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b27f1-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="b27f1-116">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="b27f1-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

