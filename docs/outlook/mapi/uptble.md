---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592340"
---
# <a name="uptble"></a><span data-ttu-id="a9e8b-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="a9e8b-103">UPTBLE</span></span>

<span data-ttu-id="a9e8b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9e8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9e8b-105">[テーブルの状態をアップロード](upload-table-state.md)する時にフォルダーの内容をアップロードするための情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="a9e8b-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a9e8b-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a9e8b-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="a9e8b-107">Members</span><span class="sxs-lookup"><span data-stu-id="a9e8b-107">Members</span></span>

 <span data-ttu-id="a9e8b-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="a9e8b-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="a9e8b-109">[out]新しいまたは変更されたアイテムの数の_cEntMod_のアップロードを追跡するためにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a9e8b-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="a9e8b-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="a9e8b-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="a9e8b-111">[out]フォルダー内の新規または変更されたアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="a9e8b-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="a9e8b-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="a9e8b-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="a9e8b-113">[out]_CEntRead_アイテムの読み取りの数をアップロードするかを追跡するためにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a9e8b-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="a9e8b-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="a9e8b-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="a9e8b-115">[out]フォルダー内のアイテムの読み取りの数です。</span><span class="sxs-lookup"><span data-stu-id="a9e8b-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="a9e8b-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="a9e8b-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="a9e8b-117">[out]アップロード_cEntDel_の数を追跡するためにインデックスには、項目が削除されます。</span><span class="sxs-lookup"><span data-stu-id="a9e8b-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="a9e8b-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="a9e8b-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="a9e8b-119">[out]フォルダー内の削除済みアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="a9e8b-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a9e8b-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9e8b-120">See also</span></span>

- [<span data-ttu-id="a9e8b-121">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a9e8b-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="a9e8b-122">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="a9e8b-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="a9e8b-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="a9e8b-123">UPTBL</span></span>](uptbl.md)

