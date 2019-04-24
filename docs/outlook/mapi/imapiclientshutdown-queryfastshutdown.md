---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350870"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="abb0f-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="abb0f-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="abb0f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abb0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abb0f-105">読み込み済みの mapi プロバイダーによって提供される高速シャットダウンのサポートを mapi サブシステムに対して照会します。</span><span class="sxs-lookup"><span data-stu-id="abb0f-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="abb0f-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="abb0f-106">Return value</span></span>

<span data-ttu-id="abb0f-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="abb0f-107">S_OK</span></span>
  
> <span data-ttu-id="abb0f-108">mapi サブシステムは、高速シャットダウンを実行するための mapi クライアントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="abb0f-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="abb0f-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="abb0f-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="abb0f-110">mapi プロバイダーは、高速シャットダウンを実行するための mapi クライアントをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="abb0f-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="abb0f-111">解説</span><span class="sxs-lookup"><span data-stu-id="abb0f-111">Remarks</span></span>

<span data-ttu-id="abb0f-112">mapi サブシステムで高速シャットダウンを実行するための mapi クライアントがサポートされているかどうかは、ユーザーの Windows レジストリ設定または mapi クライアントの高速シャットダウンの既定の動作によって異なります。</span><span class="sxs-lookup"><span data-stu-id="abb0f-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="abb0f-113">また、読み込み済みの MAPI プロバイダーが高速シャットダウンをサポートする機能によっても異なります。</span><span class="sxs-lookup"><span data-stu-id="abb0f-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="abb0f-114">詳細については、「 [Fast Shutdown User Options](fast-shutdown-user-options.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="abb0f-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="abb0f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="abb0f-115">See also</span></span>



[<span data-ttu-id="abb0f-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="abb0f-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="abb0f-117">MAPI でのクライアント シャットダウン</span><span class="sxs-lookup"><span data-stu-id="abb0f-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

