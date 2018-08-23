---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803944"
---
# <a name="skey"></a><span data-ttu-id="dde9b-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="dde9b-103">SKEY</span></span>

  
  
<span data-ttu-id="dde9b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dde9b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dde9b-105">Outlook アイテムのソースのキーです。</span><span class="sxs-lookup"><span data-stu-id="dde9b-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dde9b-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="dde9b-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="dde9b-107">Members</span><span class="sxs-lookup"><span data-stu-id="dde9b-107">Members</span></span>

 <span data-ttu-id="dde9b-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="dde9b-108">_guid_</span></span>
  
> <span data-ttu-id="dde9b-109">オブジェクトを作成するサーバーの GUID です。</span><span class="sxs-lookup"><span data-stu-id="dde9b-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dde9b-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="dde9b-110">See also</span></span>



[<span data-ttu-id="dde9b-111">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="dde9b-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="dde9b-112">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="dde9b-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="dde9b-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="dde9b-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="dde9b-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="dde9b-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="dde9b-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="dde9b-115">UPREADE</span></span>](upreade.md)

