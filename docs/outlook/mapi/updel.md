---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360488"
---
# <a name="updel"></a><span data-ttu-id="7823b-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="7823b-103">UPDEL</span></span>

  
  
<span data-ttu-id="7823b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7823b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7823b-105">ローカルストアで削除されたアイテムに関する情報。</span><span class="sxs-lookup"><span data-stu-id="7823b-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="7823b-106">この情報は、削除の状態の[アップロード](upload-delete-status-state.md)中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7823b-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7823b-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="7823b-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="7823b-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="7823b-108">Members</span></span>

 <span data-ttu-id="7823b-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="7823b-109">_pupde_</span></span>
  
>  <span data-ttu-id="7823b-110">読み上げ[updele](updele.md)エントリのベクトル。</span><span class="sxs-lookup"><span data-stu-id="7823b-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="7823b-111">_fea-cent-logging-service_</span><span class="sxs-lookup"><span data-stu-id="7823b-111">_cEnt_</span></span>
  
> <span data-ttu-id="7823b-112">読み上げ*pupde*のエントリ数。</span><span class="sxs-lookup"><span data-stu-id="7823b-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7823b-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="7823b-113">See also</span></span>



[<span data-ttu-id="7823b-114">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="7823b-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7823b-115">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="7823b-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7823b-116">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="7823b-116">MAPI Constants</span></span>](mapi-constants.md)

