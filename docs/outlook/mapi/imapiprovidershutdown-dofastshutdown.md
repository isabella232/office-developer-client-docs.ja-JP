---
title: imapiprovidershutdowndofastshutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428845"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="c9d59-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="c9d59-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="c9d59-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9d59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9d59-105">mapi プロバイダーに対して、mapi クライアントが直ちに終了していることを示します。したがって、データ損失を防止するために mapi プロバイダーは変更を保持します。</span><span class="sxs-lookup"><span data-stu-id="c9d59-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="c9d59-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="c9d59-106">Return value</span></span>

<span data-ttu-id="c9d59-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9d59-107">S_OK</span></span>
  
> <span data-ttu-id="c9d59-108">mapi プロバイダーは、mapi クライアントが直ちに終了する準備ができています。</span><span class="sxs-lookup"><span data-stu-id="c9d59-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c9d59-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="c9d59-109">See also</span></span>



[<span data-ttu-id="c9d59-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9d59-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="c9d59-111">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="c9d59-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

