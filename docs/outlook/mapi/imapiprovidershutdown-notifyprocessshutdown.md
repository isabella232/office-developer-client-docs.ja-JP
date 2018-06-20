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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cce98dc630dd9f7fa459ca31d94d012ba9a7fd85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800675"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="dae60-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="dae60-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="dae60-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dae60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dae60-105">MAPI プロバイダーをプロバイダーは、データ損失を防ぐための処置を行うことができるように、高速シャット ダウンを行う MAPI クライアントを送信することを示します。</span><span class="sxs-lookup"><span data-stu-id="dae60-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="dae60-106">�߂�l</span><span class="sxs-lookup"><span data-stu-id="dae60-106">Return value</span></span>

<span data-ttu-id="dae60-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="dae60-107">S_OK</span></span>
  
> <span data-ttu-id="dae60-108">MAPI プロバイダーがアクションを実行して、MAPI クライアントのシャット ダウン時にデータ損失を防止します。</span><span class="sxs-lookup"><span data-stu-id="dae60-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dae60-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="dae60-109">See also</span></span>



[<span data-ttu-id="dae60-110">IMAPIProviderShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dae60-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="dae60-111">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="dae60-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

