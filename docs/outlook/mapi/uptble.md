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
# <a name="uptble"></a><span data-ttu-id="94f7f-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="94f7f-103">UPTBLE</span></span>

<span data-ttu-id="94f7f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94f7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94f7f-105">アップロード テーブルの状態の間にフォルダーの内容をアップロードする [際の拡張情報](upload-table-state.md)。</span><span class="sxs-lookup"><span data-stu-id="94f7f-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="94f7f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="94f7f-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="94f7f-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="94f7f-107">Members</span></span>

 <span data-ttu-id="94f7f-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="94f7f-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="94f7f-109">[out]新しいアイテムまたは変更されたアイテムの  _cEntMod_ 番号のアップロードを追跡するインデックス。</span><span class="sxs-lookup"><span data-stu-id="94f7f-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="94f7f-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="94f7f-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="94f7f-111">[out]フォルダー内の新しいアイテムまたは変更されたアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="94f7f-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="94f7f-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="94f7f-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="94f7f-113">[out]cEntRead 読み取りアイテムの数のアップロード  _を追跡する_ インデックス。</span><span class="sxs-lookup"><span data-stu-id="94f7f-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="94f7f-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="94f7f-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="94f7f-115">[out]フォルダー内の読み取りアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="94f7f-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="94f7f-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="94f7f-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="94f7f-117">[out]cEntDel 削除済みアイテムの数  _のアップロードを_ 追跡するインデックス。</span><span class="sxs-lookup"><span data-stu-id="94f7f-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="94f7f-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="94f7f-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="94f7f-119">[out]フォルダー内の削除済みアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="94f7f-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="94f7f-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="94f7f-120">See also</span></span>

- [<span data-ttu-id="94f7f-121">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="94f7f-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="94f7f-122">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="94f7f-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="94f7f-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="94f7f-123">UPTBL</span></span>](uptbl.md)

