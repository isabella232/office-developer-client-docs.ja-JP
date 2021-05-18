---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 65ed848907e196c315e8ddb61c4afd2fe03faa18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413431"
---
# <a name="mapioffline_notify_type"></a><span data-ttu-id="df641-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="df641-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="df641-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df641-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df641-105">通知MAPIOFFLINE_NOTIFY_TYPEは、接続状態の変更が行うのか、起こっているのか、完了したのか、を識別します。</span><span class="sxs-lookup"><span data-stu-id="df641-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="df641-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="df641-106">Quick info</span></span>

<span data-ttu-id="df641-107">**[「IMAPIOfflineNotify」を参照してください](imapiofflinenotifyiunknown.md)**。</span><span class="sxs-lookup"><span data-stu-id="df641-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="df641-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="df641-108">See also</span></span>



[<span data-ttu-id="df641-109">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="df641-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="df641-110">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="df641-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="df641-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="df641-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

