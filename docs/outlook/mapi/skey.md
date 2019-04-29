---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c417e6f4412bc40e8c2ebc056514eb96f60798f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426808"
---
# <a name="skey"></a><span data-ttu-id="b34dc-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="b34dc-103">SKEY</span></span>

  
  
<span data-ttu-id="b34dc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b34dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b34dc-105">Outlook アイテムのソースキー。</span><span class="sxs-lookup"><span data-stu-id="b34dc-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b34dc-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b34dc-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="b34dc-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="b34dc-107">Members</span></span>

 <span data-ttu-id="b34dc-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="b34dc-108">_guid_</span></span>
  
> <span data-ttu-id="b34dc-109">オブジェクトを作成しているサーバーの GUID。</span><span class="sxs-lookup"><span data-stu-id="b34dc-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b34dc-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="b34dc-110">See also</span></span>



[<span data-ttu-id="b34dc-111">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="b34dc-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b34dc-112">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="b34dc-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b34dc-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="b34dc-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="b34dc-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="b34dc-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="b34dc-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="b34dc-115">UPREADE</span></span>](upreade.md)

