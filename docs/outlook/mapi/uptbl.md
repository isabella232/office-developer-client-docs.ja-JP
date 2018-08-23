---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bdfabdf02fc0fa6222418bd0fb87e9b6c17d936a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580440"
---
# <a name="uptbl"></a><span data-ttu-id="b5bf6-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="b5bf6-103">UPTBL</span></span>

<span data-ttu-id="b5bf6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5bf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5bf6-105">[テーブルの状態をアップロード](upload-table-state.md)する時にフォルダーの内容をアップロードする方法の詳細については。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b5bf6-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b5bf6-106">Quick info</span></span>

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a><span data-ttu-id="b5bf6-107">Members</span><span class="sxs-lookup"><span data-stu-id="b5bf6-107">Members</span></span>

<span data-ttu-id="b5bf6-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-108">_ulFlags_</span></span>
  
> <span data-ttu-id="b5bf6-109">[in]アップロード中に適切な動作を決定するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="b5bf6-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="b5bf6-110">UPT_OK</span></span>
    
    - <span data-ttu-id="b5bf6-111">[in]アップロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-111">[in] Upload was successful.</span></span> <span data-ttu-id="b5bf6-112">クライアントでは、フォルダーの内容をサーバーにアップロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="b5bf6-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="b5bf6-114">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="b5bf6-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-115">_pszName_</span></span>
  
> <span data-ttu-id="b5bf6-116">[out]フォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="b5bf6-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-117">_feid_</span></span>
  
> <span data-ttu-id="b5bf6-118">[out]フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="b5bf6-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-119">_uintReserved_</span></span>
  
> <span data-ttu-id="b5bf6-120">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="b5bf6-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-121">_rgte_</span></span>
  
> <span data-ttu-id="b5bf6-122">[out]フォルダーに通常 (または非表示) の項目と関連付けられている (非表示) の項目について次の情報を保持する構造体: _rgte [0]_ は通常と関連付けられているアイテムについては、 _rgte [1]_ 。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="b5bf6-123">新しいまたは変更されたアイテムの数</span><span class="sxs-lookup"><span data-stu-id="b5bf6-123">the number of new or modified items</span></span>
   - <span data-ttu-id="b5bf6-124">読み取りの項目の数</span><span class="sxs-lookup"><span data-stu-id="b5bf6-124">the number of read items</span></span> 
   - <span data-ttu-id="b5bf6-125">削除済みアイテムの数</span><span class="sxs-lookup"><span data-stu-id="b5bf6-125">the number of deleted items</span></span>
    
 <span data-ttu-id="b5bf6-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-126">_iEnt_</span></span>
  
> <span data-ttu-id="b5bf6-127">[out]_セント_で指定された変更の数をアップロードするかを追跡するためにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="b5bf6-128">_セント_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-128">_cEnt_</span></span>
  
> <span data-ttu-id="b5bf6-129">[out]フォルダーへの変更の数です。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="b5bf6-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="b5bf6-131">[out][UPMOV](upmov.md)構造体のチェーンです。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="b5bf6-132">_保持_</span><span class="sxs-lookup"><span data-stu-id="b5bf6-132">_pReserved_</span></span>
  
> <span data-ttu-id="b5bf6-133">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b5bf6-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5bf6-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5bf6-134">See also</span></span>

- [<span data-ttu-id="b5bf6-135">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="b5bf6-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="b5bf6-136">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="b5bf6-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="b5bf6-137">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="b5bf6-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="b5bf6-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="b5bf6-138">UPTBLE</span></span>](uptble.md)

