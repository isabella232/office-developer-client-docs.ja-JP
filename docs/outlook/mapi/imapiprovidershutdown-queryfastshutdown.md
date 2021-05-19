---
title: IMAPIProviderShutdownQueryFastShutdown
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418219"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="3bfe1-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="3bfe1-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="3bfe1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bfe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bfe1-105">MAPI プロバイダーに高速シャットダウンのサポートを照会します。</span><span class="sxs-lookup"><span data-stu-id="3bfe1-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="3bfe1-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="3bfe1-106">Return value</span></span>

<span data-ttu-id="3bfe1-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="3bfe1-107">S_OK</span></span>
  
> <span data-ttu-id="3bfe1-108">MAPI プロバイダーは、高速シャットダウンを実行する MAPI クライアントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3bfe1-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="3bfe1-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3bfe1-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="3bfe1-110">MAPI プロバイダーは、高速シャットダウンを実行する MAPI クライアントをサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="3bfe1-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3bfe1-111">注釈</span><span class="sxs-lookup"><span data-stu-id="3bfe1-111">Remarks</span></span>

<span data-ttu-id="3bfe1-112">クライアントの高速シャットダウンをサポートする必要のない MAPI プロバイダーは [、IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) インターフェイスを実装し **、IMAPIProviderShutdown::QueryFastShutdown** メソッドが MAPI_E_NO_SUPPORT を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bfe1-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="3bfe1-113">MAPI Outlookとして使用すると、Outlook前にすべての外部参照が解放されるのを待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bfe1-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="3bfe1-114">高速シャットダウン用のユーザーの Windows レジストリ設定によっては **、IMAPIProviderShutdown** インターフェイスを実装しない場合でも、クライアントの高速シャットダウンが必ずしも妨げであるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="3bfe1-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bfe1-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3bfe1-115">See also</span></span>



[<span data-ttu-id="3bfe1-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bfe1-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="3bfe1-117">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="3bfe1-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

