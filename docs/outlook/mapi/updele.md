---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360544"
---
# <a name="updele"></a><span data-ttu-id="4f0f5-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="4f0f5-103">UPDELE</span></span>

<span data-ttu-id="4f0f5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f0f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f0f5-105">ローカルストアで削除されたアイテムの拡張情報。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="4f0f5-106">この情報は、削除の状態の[アップロード](upload-delete-status-state.md)中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4f0f5-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="4f0f5-107">Quick info</span></span>

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a><span data-ttu-id="4f0f5-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="4f0f5-108">Members</span></span>

<span data-ttu-id="4f0f5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f0f5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4f0f5-110">[out]/[in] アップロード中の適切な動作を決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="4f0f5-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="4f0f5-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="4f0f5-112">読み上げ項目が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="4f0f5-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="4f0f5-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="4f0f5-114">読み上げアイテムが移動されました。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="4f0f5-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="4f0f5-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="4f0f5-116">順番アップロードに成功しました。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-116">[in] Upload was successful.</span></span> <span data-ttu-id="4f0f5-117">クライアントは、情報をサーバーにアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="4f0f5-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="4f0f5-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="4f0f5-119">順番アイテムは正常に移動されました。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="4f0f5-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="4f0f5-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="4f0f5-121">順番ソースアイテムを変更済みとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="4f0f5-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="4f0f5-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="4f0f5-123">順番今すぐアップロードの状態をコミットします (エントリ 0)。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="4f0f5-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="4f0f5-124">_skey_</span></span>
  
> <span data-ttu-id="4f0f5-125">読み上げアイテムのソースキー。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="4f0f5-126">_dwreserved_</span><span class="sxs-lookup"><span data-stu-id="4f0f5-126">_dwReserved_</span></span>
  
> <span data-ttu-id="4f0f5-127">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="4f0f5-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="4f0f5-128">_binChg_</span></span>
  
> <span data-ttu-id="4f0f5-129">読み上げアイテムが移動された場合は、コピー先アイテムのキーを変更します。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="4f0f5-130">_binpcl_</span><span class="sxs-lookup"><span data-stu-id="4f0f5-130">_binPcl_</span></span>
  
> <span data-ttu-id="4f0f5-131">読み上げアイテムが移動された場合は、コピー先アイテムのリストを変更します。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="4f0f5-132">_skeydst_</span><span class="sxs-lookup"><span data-stu-id="4f0f5-132">_skeyDst_</span></span>
  
> <span data-ttu-id="4f0f5-133">読み上げアイテムが移動された場合のコピー先アイテムのソースキー。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="4f0f5-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="4f0f5-134">_pupmov_</span></span>
  
> <span data-ttu-id="4f0f5-135">読み上げアイテムが移動された場合の移動先フォルダーの情報。</span><span class="sxs-lookup"><span data-stu-id="4f0f5-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f0f5-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f0f5-136">See also</span></span>

- [<span data-ttu-id="4f0f5-137">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="4f0f5-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="4f0f5-138">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="4f0f5-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="4f0f5-139">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="4f0f5-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="4f0f5-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="4f0f5-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="4f0f5-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="4f0f5-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="4f0f5-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="4f0f5-142">UPMOV</span></span>](upmov.md)

