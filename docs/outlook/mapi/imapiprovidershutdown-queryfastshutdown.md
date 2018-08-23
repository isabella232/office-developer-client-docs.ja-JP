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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800701"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="9da89-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="9da89-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="9da89-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9da89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9da89-105">クエリは高速シャット ダウンの MAPI プロバイダーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9da89-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="9da89-106">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9da89-106">Return value</span></span>

<span data-ttu-id="9da89-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="9da89-107">S_OK</span></span>
  
> <span data-ttu-id="9da89-108">MAPI プロバイダーには、高速シャット ダウンを実行するのには MAPI クライアントがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9da89-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="9da89-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9da89-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="9da89-110">MAPI プロバイダーは、高速シャット ダウンを実行するのには MAPI クライアントをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="9da89-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9da89-111">注釈</span><span class="sxs-lookup"><span data-stu-id="9da89-111">Remarks</span></span>

<span data-ttu-id="9da89-112">クライアントの高速シャット ダウンをサポートするために必要としない MAPI プロバイダーの[IMAPIProviderShutdown](imapiprovidershutdowniunknown.md)インターフェイスを実装し、MAPI_E_NO_SUPPORT を返す**IMAPIProviderShutdown::QueryFastShutdown**メソッドがある必要がありますも。</span><span class="sxs-lookup"><span data-stu-id="9da89-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="9da89-113">MAPI クライアントとして outlook でこのすべての外部参照を終了する前に解放するまで待機するように Outlook が発生します。</span><span class="sxs-lookup"><span data-stu-id="9da89-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="9da89-114">によって**IMAPIProviderShutdown**インターフェイスを実装しない、高速シャット ダウンのレジストリ設定が必ずしもユーザーの Windows クライアントの高速シャット ダウンを防止します。</span><span class="sxs-lookup"><span data-stu-id="9da89-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9da89-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="9da89-115">See also</span></span>



[<span data-ttu-id="9da89-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9da89-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="9da89-117">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="9da89-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

