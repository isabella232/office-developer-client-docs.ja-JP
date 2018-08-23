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
ms.openlocfilehash: faa061ae323dd744d12e4f9abec713c71379feba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563472"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="c2b84-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="c2b84-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="c2b84-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2b84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2b84-105">示します MAPI プロバイダーに MAPI クライアントが、すぐに終了している MAPI プロバイダーがデータの損失を防ぐために加えられた変更を永続化できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c2b84-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="c2b84-106">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c2b84-106">Return value</span></span>

<span data-ttu-id="c2b84-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2b84-107">S_OK</span></span>
  
> <span data-ttu-id="c2b84-108">MAPI プロバイダーを即座に終了するのには MAPI クライアントの準備ができました。</span><span class="sxs-lookup"><span data-stu-id="c2b84-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c2b84-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2b84-109">See also</span></span>



[<span data-ttu-id="c2b84-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2b84-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="c2b84-111">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="c2b84-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

