---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351360"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="eae81-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="eae81-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="eae81-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eae81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eae81-105">シャットダウンを続行する MAPI クライアントの意図を示します。</span><span class="sxs-lookup"><span data-stu-id="eae81-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="eae81-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="eae81-106">Return value</span></span>

<span data-ttu-id="eae81-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="eae81-107">S_OK</span></span>
  
> <span data-ttu-id="eae81-108">mapi サブシステムは、読み込み済みの mapi プロバイダーに、mapi クライアントが高速シャットダウンを行うことになることを通知しようとしました。</span><span class="sxs-lookup"><span data-stu-id="eae81-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eae81-109">解説</span><span class="sxs-lookup"><span data-stu-id="eae81-109">Remarks</span></span>

<span data-ttu-id="eae81-110">mapi クライアントの高速シャットダウンからのデータ損失を回避するために、mapi クライアントは、 **IMAPIClientShutdown:: notifyprocessshutdown**および[IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md)メソッドを呼び出す必要があります。これは、次の mapi サブシステムによって返される S_OK 結果に基づいています。[IMAPIClientShutdown:: queryfastshutdown](imapiclientshutdown-queryfastshutdown.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="eae81-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="eae81-111">詳細については、「[ファストシャットダウンのベストプラクティス](best-practices-for-fast-shutdown.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eae81-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eae81-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="eae81-112">See also</span></span>



[<span data-ttu-id="eae81-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eae81-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="eae81-114">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="eae81-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

