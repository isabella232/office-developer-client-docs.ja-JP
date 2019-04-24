---
title: imapiprovidershutdownqueryfastshutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338487"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="47d2e-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="47d2e-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="47d2e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47d2e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47d2e-105">MAPI プロバイダーに対して、高速シャットダウンのサポートを照会します。</span><span class="sxs-lookup"><span data-stu-id="47d2e-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="47d2e-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="47d2e-106">Return value</span></span>

<span data-ttu-id="47d2e-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="47d2e-107">S_OK</span></span>
  
> <span data-ttu-id="47d2e-108">mapi プロバイダーは、高速シャットダウンを実行するための mapi クライアントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="47d2e-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="47d2e-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="47d2e-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="47d2e-110">mapi プロバイダーは、高速シャットダウンを実行するための mapi クライアントをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="47d2e-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47d2e-111">解説</span><span class="sxs-lookup"><span data-stu-id="47d2e-111">Remarks</span></span>

<span data-ttu-id="47d2e-112">クライアントの高速シャットダウンをサポートする必要がない MAPI プロバイダーは、まだ[imapiprovidershutdown](imapiprovidershutdowniunknown.md)インターフェイスを実装していて、 **imapiprovidershutdown:: queryfastshutdown**メソッドが MAPI_E_NO_SUPPORT を返すようにしてください。</span><span class="sxs-lookup"><span data-stu-id="47d2e-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="47d2e-113">outlook を MAPI クライアントとして使用する場合、outlook は、すべての外部参照が終了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="47d2e-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="47d2e-114">高速シャットダウンのためのユーザーの Windows レジストリ設定によっては、 **imapiprovidershutdown**インターフェイスを実装していないと、クライアントの高速シャットダウンが必ずしも妨げられるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="47d2e-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47d2e-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="47d2e-115">See also</span></span>



[<span data-ttu-id="47d2e-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47d2e-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="47d2e-117">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="47d2e-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

