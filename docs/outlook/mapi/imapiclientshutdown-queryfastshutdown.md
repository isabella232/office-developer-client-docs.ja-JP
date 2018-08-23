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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 059d0d4427a8f2d68795a671d77fb9e3d84294f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800463"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="f5c3b-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="f5c3b-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="f5c3b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f5c3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f5c3b-105">クエリ、MAPI サブシステムの高速シャット ダウンをサポートして読み込まれている MAPI プロバイダーによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="f5c3b-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="f5c3b-106">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f5c3b-106">Return value</span></span>

<span data-ttu-id="f5c3b-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5c3b-107">S_OK</span></span>
  
> <span data-ttu-id="f5c3b-108">MAPI サブシステムには、高速シャット ダウンを実行するのには MAPI クライアントがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f5c3b-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="f5c3b-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f5c3b-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="f5c3b-110">MAPI プロバイダーは、高速シャット ダウンを実行するのには MAPI クライアントをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f5c3b-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5c3b-111">注釈</span><span class="sxs-lookup"><span data-stu-id="f5c3b-111">Remarks</span></span>

<span data-ttu-id="f5c3b-112">MAPI サブシステムが高速シャット ダウンを実行するのには MAPI クライアントをサポートしているかどうかは、ユーザーの Windows レジストリ設定または高速シャット ダウンのために MAPI クライアントの既定の動作によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f5c3b-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="f5c3b-113">高速シャット ダウンをサポートするために読み込まれている MAPI プロバイダーの機能によっても異なります。</span><span class="sxs-lookup"><span data-stu-id="f5c3b-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="f5c3b-114">詳細については、[高速シャット ダウンのユーザー オプション](fast-shutdown-user-options.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5c3b-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5c3b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5c3b-115">See also</span></span>



[<span data-ttu-id="f5c3b-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5c3b-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="f5c3b-117">Mapi クライアントのシャット ダウン</span><span class="sxs-lookup"><span data-stu-id="f5c3b-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

