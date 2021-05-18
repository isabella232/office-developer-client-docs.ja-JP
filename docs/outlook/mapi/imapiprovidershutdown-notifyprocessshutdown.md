---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405248"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="02dcd-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="02dcd-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="02dcd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02dcd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02dcd-105">MAPI クライアントが高速シャットダウンを実行し、プロバイダーがデータ損失を防止するアクションを実行できるよう、MAPI プロバイダーに対して示します。</span><span class="sxs-lookup"><span data-stu-id="02dcd-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="02dcd-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="02dcd-106">Return value</span></span>

<span data-ttu-id="02dcd-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="02dcd-107">S_OK</span></span>
  
> <span data-ttu-id="02dcd-108">MAPI プロバイダーは、MAPI クライアントがシャットダウンするときにデータ損失を防止するアクションを実行しています。</span><span class="sxs-lookup"><span data-stu-id="02dcd-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02dcd-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="02dcd-109">See also</span></span>



[<span data-ttu-id="02dcd-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02dcd-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="02dcd-111">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="02dcd-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

