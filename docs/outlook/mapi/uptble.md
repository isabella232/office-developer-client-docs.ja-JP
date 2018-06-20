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
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804200"
---
# <a name="uptble"></a><span data-ttu-id="951a3-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="951a3-103">UPTBLE</span></span>

<span data-ttu-id="951a3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="951a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="951a3-105">[テーブルの状態をアップロード](upload-table-state.md)する時にフォルダーの内容をアップロードするための情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="951a3-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="951a3-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="951a3-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="951a3-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="951a3-107">Members</span></span>

 <span data-ttu-id="951a3-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="951a3-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="951a3-109">[out]新しいまたは変更されたアイテムの数の_cEntMod_のアップロードを追跡するためにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="951a3-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="951a3-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="951a3-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="951a3-111">[out]フォルダー内の新規または変更されたアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="951a3-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="951a3-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="951a3-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="951a3-113">[out]_CEntRead_アイテムの読み取りの数をアップロードするかを追跡するためにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="951a3-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="951a3-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="951a3-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="951a3-115">[out]フォルダー内のアイテムの読み取りの数です。</span><span class="sxs-lookup"><span data-stu-id="951a3-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="951a3-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="951a3-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="951a3-117">[out]アップロード_cEntDel_の数を追跡するためにインデックスには、項目が削除されます。</span><span class="sxs-lookup"><span data-stu-id="951a3-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="951a3-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="951a3-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="951a3-119">[out]フォルダー内の削除済みアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="951a3-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="951a3-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="951a3-120">See also</span></span>

- [<span data-ttu-id="951a3-121">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="951a3-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="951a3-122">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="951a3-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="951a3-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="951a3-123">UPTBL</span></span>](uptbl.md)

