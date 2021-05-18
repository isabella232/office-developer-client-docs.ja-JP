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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408685"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="318cd-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="318cd-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="318cd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="318cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="318cd-105">MAPI クライアントがクライアント プロセスを直ちに終了する意図を示します。</span><span class="sxs-lookup"><span data-stu-id="318cd-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="318cd-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="318cd-106">Return value</span></span>

<span data-ttu-id="318cd-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="318cd-107">S_OK</span></span>
  
> <span data-ttu-id="318cd-108">MAPI サブシステムは、MAPI クライアントが直ちに終了し、MAPI プロバイダーがクライアント出口の準備ができていることを読み込んだ MAPI プロバイダーに示しています。</span><span class="sxs-lookup"><span data-stu-id="318cd-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="318cd-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="318cd-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="318cd-110">MAPI サブシステムでは、クライアントの高速シャットダウンはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="318cd-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="318cd-111">注釈</span><span class="sxs-lookup"><span data-stu-id="318cd-111">Remarks</span></span>

<span data-ttu-id="318cd-112">MAPI クライアントの高速シャットダウンによるデータ損失を回避するために、MAPI クライアントは[IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md)メソッドと IMAPIClientShutdown::D oFastShutdown メソッドを[IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md)メソッドの MAPI サブシステムによって返される S_OK 結果に基づいて呼び出す必要があります。 </span><span class="sxs-lookup"><span data-stu-id="318cd-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="318cd-113">詳細については、「高速シャットダウン [のベスト プラクティス」を参照してください](best-practices-for-fast-shutdown.md)。</span><span class="sxs-lookup"><span data-stu-id="318cd-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="318cd-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="318cd-114">See also</span></span>



[<span data-ttu-id="318cd-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="318cd-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="318cd-116">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="318cd-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

