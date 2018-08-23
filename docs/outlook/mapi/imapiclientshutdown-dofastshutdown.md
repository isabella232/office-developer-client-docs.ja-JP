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
ms.openlocfilehash: 41c4ee65ce6ae8f2e0d978f1e2bd95adb4f5872a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575176"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="30d17-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="30d17-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="30d17-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30d17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30d17-105">MAPI クライアントのクライアントのプロセスを即座に終了するという意図を示しています。</span><span class="sxs-lookup"><span data-stu-id="30d17-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="30d17-106">�߂�l</span><span class="sxs-lookup"><span data-stu-id="30d17-106">Return value</span></span>

<span data-ttu-id="30d17-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="30d17-107">S_OK</span></span>
  
> <span data-ttu-id="30d17-108">MAPI クライアントは、すぐに終了して、MAPI プロバイダーは、クライアントの終了の準備ができて読み込まれている MAPI プロバイダーに、MAPI サブシステムを示しています。</span><span class="sxs-lookup"><span data-stu-id="30d17-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="30d17-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="30d17-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="30d17-110">MAPI サブシステムは、クライアントの高速シャット ダウンをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="30d17-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30d17-111">注釈</span><span class="sxs-lookup"><span data-stu-id="30d17-111">Remarks</span></span>

<span data-ttu-id="30d17-112">MAPI クライアントの高速シャット ダウンからのデータの損失を避けるためには、MAPI クライアントが、MAPI サブシステムによって返される S_OK の結果に基づく[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)と**IMAPIClientShutdown::DoFastShutdown**のメソッドを呼び出す必要があります。[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="30d17-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="30d17-113">詳細については、[高速シャット ダウンのベスト ・ プラクティス](best-practices-for-fast-shutdown.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30d17-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30d17-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="30d17-114">See also</span></span>



[<span data-ttu-id="30d17-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30d17-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="30d17-116">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="30d17-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

