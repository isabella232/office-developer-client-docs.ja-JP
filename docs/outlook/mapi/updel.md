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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436801"
---
# <a name="updel"></a><span data-ttu-id="718e5-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="718e5-103">UPDEL</span></span>

  
  
<span data-ttu-id="718e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="718e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="718e5-105">ローカル ストアで削除されたアイテムの情報。</span><span class="sxs-lookup"><span data-stu-id="718e5-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="718e5-106">この情報は、アップロードの削除状態 [の間に使用されます](upload-delete-status-state.md)。</span><span class="sxs-lookup"><span data-stu-id="718e5-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="718e5-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="718e5-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="718e5-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="718e5-108">Members</span></span>

 <span data-ttu-id="718e5-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="718e5-109">_pupde_</span></span>
  
>  <span data-ttu-id="718e5-110">[out] [UPDELE エントリの](updele.md) ベクトル。</span><span class="sxs-lookup"><span data-stu-id="718e5-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="718e5-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="718e5-111">_cEnt_</span></span>
  
> <span data-ttu-id="718e5-112">[out]pupde の  *エントリの数*  。</span><span class="sxs-lookup"><span data-stu-id="718e5-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="718e5-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="718e5-113">See also</span></span>



[<span data-ttu-id="718e5-114">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="718e5-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="718e5-115">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="718e5-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="718e5-116">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="718e5-116">MAPI Constants</span></span>](mapi-constants.md)

