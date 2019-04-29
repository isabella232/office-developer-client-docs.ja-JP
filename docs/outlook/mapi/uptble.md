---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413841"
---
# <a name="uptble"></a><span data-ttu-id="1ba4e-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="1ba4e-103">UPTBLE</span></span>

<span data-ttu-id="1ba4e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ba4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ba4e-105">[テーブルのアップロード状態](upload-table-state.md)中にフォルダーのコンテンツをアップロードするための拡張情報。</span><span class="sxs-lookup"><span data-stu-id="1ba4e-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1ba4e-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1ba4e-106">Quick info</span></span>

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="1ba4e-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="1ba4e-107">Members</span></span>

 <span data-ttu-id="1ba4e-108">_ientmod_</span><span class="sxs-lookup"><span data-stu-id="1ba4e-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="1ba4e-109">読み上げ_cEntMod_数の新規または変更されたアイテムのアップロードを追跡するインデックス。</span><span class="sxs-lookup"><span data-stu-id="1ba4e-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="1ba4e-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="1ba4e-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="1ba4e-111">読み上げフォルダー内の新規または変更されたアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="1ba4e-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="1ba4e-112">_ientread_</span><span class="sxs-lookup"><span data-stu-id="1ba4e-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="1ba4e-113">読み上げ_cEntRead_の読み取りアイテム数のアップロードを追跡するインデックス。</span><span class="sxs-lookup"><span data-stu-id="1ba4e-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="1ba4e-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="1ba4e-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="1ba4e-115">読み上げフォルダー内の読み取り済みアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="1ba4e-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="1ba4e-116">_ientdel_</span><span class="sxs-lookup"><span data-stu-id="1ba4e-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="1ba4e-117">読み上げ_cEntDel_の削除済みアイテムの数をアップロードする追跡対象のインデックス。</span><span class="sxs-lookup"><span data-stu-id="1ba4e-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="1ba4e-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="1ba4e-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="1ba4e-119">読み上げフォルダー内の削除済みアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="1ba4e-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1ba4e-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ba4e-120">See also</span></span>

- [<span data-ttu-id="1ba4e-121">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="1ba4e-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="1ba4e-122">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="1ba4e-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1ba4e-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="1ba4e-123">UPTBL</span></span>](uptbl.md)

