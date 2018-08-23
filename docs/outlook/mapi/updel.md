---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804171"
---
# <a name="updel"></a><span data-ttu-id="b9450-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="b9450-103">UPDEL</span></span>

  
  
<span data-ttu-id="b9450-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9450-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9450-105">ローカル ストアで削除済みアイテムの情報です。</span><span class="sxs-lookup"><span data-stu-id="b9450-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="b9450-106">[アップロード ステータスの状態を削除](upload-delete-status-state.md)する時にこの情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b9450-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b9450-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b9450-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="b9450-108">Members</span><span class="sxs-lookup"><span data-stu-id="b9450-108">Members</span></span>

 <span data-ttu-id="b9450-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="b9450-109">_pupde_</span></span>
  
>  <span data-ttu-id="b9450-110">[out][UPDELE](updele.md)エントリのベクターです。</span><span class="sxs-lookup"><span data-stu-id="b9450-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="b9450-111">_セント_</span><span class="sxs-lookup"><span data-stu-id="b9450-111">_cEnt_</span></span>
  
> <span data-ttu-id="b9450-112">[out]*Pupde*内のエントリの数です。</span><span class="sxs-lookup"><span data-stu-id="b9450-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b9450-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9450-113">See also</span></span>



[<span data-ttu-id="b9450-114">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="b9450-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b9450-115">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="b9450-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b9450-116">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="b9450-116">MAPI Constants</span></span>](mapi-constants.md)

