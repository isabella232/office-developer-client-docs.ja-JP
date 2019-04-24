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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350905"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="ed22d-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="ed22d-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="ed22d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed22d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed22d-105">クライアントプロセスをすぐに終了する MAPI クライアントの意図を示します。</span><span class="sxs-lookup"><span data-stu-id="ed22d-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="ed22d-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="ed22d-106">Return value</span></span>

<span data-ttu-id="ed22d-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed22d-107">S_OK</span></span>
  
> <span data-ttu-id="ed22d-108">mapi サブシステムは、mapi クライアントが直ちに終了し、mapi プロバイダーがクライアントの終了の準備ができていることを、読み込み済みの mapi プロバイダーに示しています。</span><span class="sxs-lookup"><span data-stu-id="ed22d-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="ed22d-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ed22d-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="ed22d-110">MAPI サブシステムは、クライアントの高速シャットダウンをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="ed22d-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed22d-111">解説</span><span class="sxs-lookup"><span data-stu-id="ed22d-111">Remarks</span></span>

<span data-ttu-id="ed22d-112">mapi クライアントの高速シャットダウンからのデータ損失を回避するために、mapi クライアントは、 [IMAPIClientShutdown:: notifyprocessshutdown](imapiclientshutdown-notifyprocessshutdown.md)および**IMAPIClientShutdown::D ofastshutdown**メソッドを呼び出す必要があります。これは、次の mapi サブシステムによって返される S_OK 結果に基づいています。[IMAPIClientShutdown:: queryfastshutdown](imapiclientshutdown-queryfastshutdown.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="ed22d-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="ed22d-113">詳細については、「[ファストシャットダウンのベストプラクティス](best-practices-for-fast-shutdown.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed22d-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed22d-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed22d-114">See also</span></span>



[<span data-ttu-id="ed22d-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed22d-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="ed22d-116">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="ed22d-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

