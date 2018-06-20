---
title: IMAPIProviderShutdownDoFastShutdown
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7c38f0650315495875357862f5fa7fe138d2c61b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800654"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="ef266-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="ef266-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="ef266-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef266-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef266-105">示します MAPI プロバイダーに MAPI クライアントが、すぐに終了している MAPI プロバイダーがデータの損失を防ぐために加えられた変更を永続化できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ef266-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="ef266-106">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ef266-106">Return value</span></span>

<span data-ttu-id="ef266-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef266-107">S_OK</span></span>
  
> <span data-ttu-id="ef266-108">MAPI プロバイダーを即座に終了するのには MAPI クライアントの準備ができました。</span><span class="sxs-lookup"><span data-stu-id="ef266-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ef266-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="ef266-109">See also</span></span>



[<span data-ttu-id="ef266-110">IMAPIProviderShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef266-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="ef266-111">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="ef266-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

