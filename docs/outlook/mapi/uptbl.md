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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338858"
---
# <a name="uptbl"></a><span data-ttu-id="23326-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="23326-103">UPTBL</span></span>

<span data-ttu-id="23326-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23326-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23326-105">[テーブルのアップロード状態](upload-table-state.md)中にフォルダーのコンテンツをアップロードするための情報。</span><span class="sxs-lookup"><span data-stu-id="23326-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="23326-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="23326-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="23326-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="23326-107">Members</span></span>

<span data-ttu-id="23326-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="23326-108">_ulFlags_</span></span>
  
> <span data-ttu-id="23326-109">順番アップロード中の適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="23326-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="23326-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="23326-110">UPT_OK</span></span>
    
    - <span data-ttu-id="23326-111">順番アップロードに成功しました。</span><span class="sxs-lookup"><span data-stu-id="23326-111">[in] Upload was successful.</span></span> <span data-ttu-id="23326-112">クライアントは、フォルダーの内容をサーバーにアップロードした後に、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="23326-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="23326-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="23326-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="23326-114">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="23326-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="23326-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="23326-115">_pszName_</span></span>
  
> <span data-ttu-id="23326-116">[out] フォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="23326-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="23326-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="23326-117">_feid_</span></span>
  
> <span data-ttu-id="23326-118">[out] フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="23326-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="23326-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="23326-119">_uintReserved_</span></span>
  
> <span data-ttu-id="23326-120">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="23326-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="23326-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="23326-121">_rgte_</span></span>
  
> <span data-ttu-id="23326-122">読み上げ_rgte [0]_ が通常のアイテムに対して、および関連付けられている (または非表示の) アイテムに対して次の情報を保持する構造。 _rgte [1]_ は関連アイテム用です。</span><span class="sxs-lookup"><span data-stu-id="23326-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="23326-123">新規または変更されたアイテムの数</span><span class="sxs-lookup"><span data-stu-id="23326-123">the number of new or modified items</span></span>
   - <span data-ttu-id="23326-124">読み取りアイテム数</span><span class="sxs-lookup"><span data-stu-id="23326-124">the number of read items</span></span> 
   - <span data-ttu-id="23326-125">削除済みアイテムの数</span><span class="sxs-lookup"><span data-stu-id="23326-125">the number of deleted items</span></span>
    
 <span data-ttu-id="23326-126">_ient_</span><span class="sxs-lookup"><span data-stu-id="23326-126">_iEnt_</span></span>
  
> <span data-ttu-id="23326-127">読み上げで指定された変更数をアップロードする__ 追跡対象のインデックス。</span><span class="sxs-lookup"><span data-stu-id="23326-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="23326-128">_fea-cent-logging-service_</span><span class="sxs-lookup"><span data-stu-id="23326-128">_cEnt_</span></span>
  
> <span data-ttu-id="23326-129">読み上げフォルダーに対する変更の数。</span><span class="sxs-lookup"><span data-stu-id="23326-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="23326-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="23326-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="23326-131">読み上げ[upmov](upmov.md)構造体のチェーン。</span><span class="sxs-lookup"><span data-stu-id="23326-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="23326-132">_保持され_</span><span class="sxs-lookup"><span data-stu-id="23326-132">_pReserved_</span></span>
  
> <span data-ttu-id="23326-133">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="23326-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23326-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="23326-134">See also</span></span>

- [<span data-ttu-id="23326-135">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="23326-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="23326-136">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="23326-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="23326-137">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="23326-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="23326-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="23326-138">UPTBLE</span></span>](uptble.md)

