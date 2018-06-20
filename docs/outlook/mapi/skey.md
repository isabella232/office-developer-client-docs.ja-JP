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
# <a name="skey"></a><span data-ttu-id="a8544-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="a8544-103">SKEY</span></span>

  
  
<span data-ttu-id="a8544-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8544-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8544-105">Outlook アイテムのソースのキーです。</span><span class="sxs-lookup"><span data-stu-id="a8544-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8544-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a8544-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="a8544-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="a8544-107">Members</span></span>

 <span data-ttu-id="a8544-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="a8544-108">_guid_</span></span>
  
> <span data-ttu-id="a8544-109">オブジェクトを作成するサーバーの GUID です。</span><span class="sxs-lookup"><span data-stu-id="a8544-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8544-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8544-110">See also</span></span>



[<span data-ttu-id="a8544-111">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a8544-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a8544-112">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="a8544-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a8544-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="a8544-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="a8544-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="a8544-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="a8544-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="a8544-115">UPREADE</span></span>](upreade.md)

