---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4dd60ffe305d27db2c9118e11cccf692652d0d27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804172"
---
# <a name="updele"></a><span data-ttu-id="3a1ea-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="3a1ea-103">UPDELE</span></span>

<span data-ttu-id="3a1ea-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a1ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a1ea-105">ローカル ストアで削除済みアイテムの情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="3a1ea-106">[アップロード ステータスの状態を削除](upload-delete-status-state.md)する時にこの情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3a1ea-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3a1ea-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="3a1ea-108">Members</span><span class="sxs-lookup"><span data-stu-id="3a1ea-108">Members</span></span>

<span data-ttu-id="3a1ea-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3a1ea-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3a1ea-110">[out]/[in] アップロード中に、適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="3a1ea-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="3a1ea-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="3a1ea-112">[out]項目に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="3a1ea-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="3a1ea-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="3a1ea-114">[out]項目移動されました。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="3a1ea-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="3a1ea-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="3a1ea-116">[in]アップロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-116">[in] Upload was successful.</span></span> <span data-ttu-id="3a1ea-117">クライアントでは、情報をサーバーにアップロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="3a1ea-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="3a1ea-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="3a1ea-119">[in]項目が正常に移動されました。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="3a1ea-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="3a1ea-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="3a1ea-121">[in]変更、ソース項目をマークします。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="3a1ea-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="3a1ea-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="3a1ea-123">[in]アップロード状態ようになりました (項目 0) をコミットします。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="3a1ea-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="3a1ea-124">_skey_</span></span>
  
> <span data-ttu-id="3a1ea-125">[out]ソース項目のキー。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="3a1ea-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="3a1ea-126">_dwReserved_</span></span>
  
> <span data-ttu-id="3a1ea-127">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="3a1ea-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="3a1ea-128">_binChg_</span></span>
  
> <span data-ttu-id="3a1ea-129">[out]項目が移動された場合は、同期先項目のキーを変更します。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="3a1ea-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="3a1ea-130">_binPcl_</span></span>
  
> <span data-ttu-id="3a1ea-131">[out]項目が移動された場合は、同期先項目の一覧を変更します。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="3a1ea-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="3a1ea-132">_skeyDst_</span></span>
  
> <span data-ttu-id="3a1ea-133">[out]同期先項目の項目のソースのキーに移動されました。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="3a1ea-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="3a1ea-134">_pupmov_</span></span>
  
> <span data-ttu-id="3a1ea-135">[out]アイテムのコピー先フォルダーの情報を移動するとします。</span><span class="sxs-lookup"><span data-stu-id="3a1ea-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a1ea-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a1ea-136">See also</span></span>

- [<span data-ttu-id="3a1ea-137">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="3a1ea-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="3a1ea-138">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="3a1ea-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="3a1ea-139">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="3a1ea-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="3a1ea-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="3a1ea-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="3a1ea-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="3a1ea-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="3a1ea-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="3a1ea-142">UPMOV</span></span>](upmov.md)

