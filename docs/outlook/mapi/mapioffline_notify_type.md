---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e7120b843eae8df70cb2c4f9cbf581dcf0e09c11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566888"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="4142f-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="4142f-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="4142f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4142f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4142f-105">通知の MAPIOFFLINE_NOTIFY_TYPE では、接続状態の変更を実行しようとしていますが行われて、または完了した場合を識別します。</span><span class="sxs-lookup"><span data-stu-id="4142f-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4142f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="4142f-106">Quick info</span></span>

<span data-ttu-id="4142f-107">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4142f-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="4142f-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="4142f-108">See also</span></span>



[<span data-ttu-id="4142f-109">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="4142f-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="4142f-110">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="4142f-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4142f-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="4142f-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

