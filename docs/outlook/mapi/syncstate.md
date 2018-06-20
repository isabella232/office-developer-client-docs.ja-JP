---
title: 同期状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 080556a7ed4530bb96db20fd96d9dda86672a720
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804093"
---
# <a name="syncstate"></a><span data-ttu-id="d9e96-103">同期状態</span><span class="sxs-lookup"><span data-stu-id="d9e96-103">SYNCSTATE</span></span>

<span data-ttu-id="d9e96-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9e96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9e96-105">この構造体は、レプリケーションの状態機械の状態を定義します。</span><span class="sxs-lookup"><span data-stu-id="d9e96-105">This structure defines the states for the replication state machine.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d9e96-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d9e96-106">Quick info</span></span>

```cpp
typedef enum { 
    LR_SYNC_IDLE = 0, 
    LR_SYNC, 
    LR_SYNC_UPLOAD_HIERARCHY, 
    LR_SYNC_UPLOAD_FOLDER, 
    LR_SYNC_CONTENTS, 
    LR_SYNC_UPLOAD_TABLE, 
    LR_SYNC_UPLOAD_MESSAGE, 
    LR_SYNC_UPLOAD_MESSAGE_READ = 8, 
    LR_SYNC_UPLOAD_MESSAGE_DEL, 
    LR_SYNC_DOWNLOAD_HIERARCHY, 
    LR_SYNC_DOWNLOAD_TABLE, 
    LR_SYNC_DOWNLOAD_HEADER = 17 
} SYNCSTATE; 

```

## <a name="see-also"></a><span data-ttu-id="d9e96-107">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9e96-107">See also</span></span>

- [<span data-ttu-id="d9e96-108">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="d9e96-108">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="d9e96-109">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="d9e96-109">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d9e96-110">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="d9e96-110">MAPI Constants</span></span>](mapi-constants.md)

