---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438114"
---
# <a name="uptbl"></a><span data-ttu-id="edf6b-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="edf6b-103">UPTBL</span></span>

<span data-ttu-id="edf6b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edf6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edf6b-105">アップロード テーブルの状態の間にフォルダーの内容を [アップロードする場合の情報](upload-table-state.md)です。</span><span class="sxs-lookup"><span data-stu-id="edf6b-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="edf6b-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="edf6b-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="edf6b-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="edf6b-107">Members</span></span>

<span data-ttu-id="edf6b-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="edf6b-108">_ulFlags_</span></span>
  
> <span data-ttu-id="edf6b-109">[in]アップロード中の適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="edf6b-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="edf6b-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="edf6b-110">UPT_OK</span></span>
    
    - <span data-ttu-id="edf6b-111">[in]アップロード成功しました。</span><span class="sxs-lookup"><span data-stu-id="edf6b-111">[in] Upload was successful.</span></span> <span data-ttu-id="edf6b-112">クライアントは、フォルダーの内容をサーバーにアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="edf6b-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="edf6b-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="edf6b-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="edf6b-114">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="edf6b-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="edf6b-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="edf6b-115">_pszName_</span></span>
  
> <span data-ttu-id="edf6b-116">[out] フォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="edf6b-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="edf6b-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="edf6b-117">_feid_</span></span>
  
> <span data-ttu-id="edf6b-118">[out] フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="edf6b-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="edf6b-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="edf6b-119">_uintReserved_</span></span>
  
> <span data-ttu-id="edf6b-120">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="edf6b-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="edf6b-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="edf6b-121">_rgte_</span></span>
  
> <span data-ttu-id="edf6b-122">[out]フォルダー内の通常の (または非表示ではない) アイテムと関連付けられた (または非表示の) アイテムに関する次の情報を保持する構造:  _rgte[0]_ は通常のアイテム用で  _、rgte[1]_ は関連付けられたアイテム用です。</span><span class="sxs-lookup"><span data-stu-id="edf6b-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="edf6b-123">新規または変更されたアイテムの数</span><span class="sxs-lookup"><span data-stu-id="edf6b-123">the number of new or modified items</span></span>
   - <span data-ttu-id="edf6b-124">読み取りアイテムの数</span><span class="sxs-lookup"><span data-stu-id="edf6b-124">the number of read items</span></span> 
   - <span data-ttu-id="edf6b-125">削除済みアイテムの数</span><span class="sxs-lookup"><span data-stu-id="edf6b-125">the number of deleted items</span></span>
    
 <span data-ttu-id="edf6b-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="edf6b-126">_iEnt_</span></span>
  
> <span data-ttu-id="edf6b-127">[out]cEnt で指定された変更の数のアップロードを追跡する  _インデックス_ です。</span><span class="sxs-lookup"><span data-stu-id="edf6b-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="edf6b-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="edf6b-128">_cEnt_</span></span>
  
> <span data-ttu-id="edf6b-129">[out]フォルダーに対する変更の数。</span><span class="sxs-lookup"><span data-stu-id="edf6b-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="edf6b-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="edf6b-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="edf6b-131">[out] [UPMOV 構造の](upmov.md) チェーン。</span><span class="sxs-lookup"><span data-stu-id="edf6b-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="edf6b-132">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="edf6b-132">_pReserved_</span></span>
  
> <span data-ttu-id="edf6b-133">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="edf6b-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="edf6b-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="edf6b-134">See also</span></span>

- [<span data-ttu-id="edf6b-135">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="edf6b-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="edf6b-136">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="edf6b-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="edf6b-137">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="edf6b-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="edf6b-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="edf6b-138">UPTBLE</span></span>](uptble.md)

