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
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566587"
---
# <a name="updele"></a><span data-ttu-id="e3f82-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="e3f82-103">UPDELE</span></span>

<span data-ttu-id="e3f82-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3f82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3f82-105">ローカル ストアで削除済みアイテムの情報を拡張します。</span><span class="sxs-lookup"><span data-stu-id="e3f82-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="e3f82-106">[アップロード ステータスの状態を削除](upload-delete-status-state.md)する時にこの情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e3f82-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e3f82-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e3f82-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="e3f82-108">Members</span><span class="sxs-lookup"><span data-stu-id="e3f82-108">Members</span></span>

<span data-ttu-id="e3f82-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3f82-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e3f82-110">[out]/[in] アップロード中に、適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="e3f82-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="e3f82-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="e3f82-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="e3f82-112">[out]項目に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="e3f82-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="e3f82-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="e3f82-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="e3f82-114">[out]項目移動されました。</span><span class="sxs-lookup"><span data-stu-id="e3f82-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="e3f82-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="e3f82-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="e3f82-116">[in]アップロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="e3f82-116">[in] Upload was successful.</span></span> <span data-ttu-id="e3f82-117">クライアントでは、情報をサーバーにアップロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="e3f82-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="e3f82-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="e3f82-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="e3f82-119">[in]項目が正常に移動されました。</span><span class="sxs-lookup"><span data-stu-id="e3f82-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="e3f82-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="e3f82-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="e3f82-121">[in]変更、ソース項目をマークします。</span><span class="sxs-lookup"><span data-stu-id="e3f82-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="e3f82-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="e3f82-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="e3f82-123">[in]アップロード状態ようになりました (項目 0) をコミットします。</span><span class="sxs-lookup"><span data-stu-id="e3f82-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="e3f82-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="e3f82-124">_skey_</span></span>
  
> <span data-ttu-id="e3f82-125">[out]ソース項目のキー。</span><span class="sxs-lookup"><span data-stu-id="e3f82-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="e3f82-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="e3f82-126">_dwReserved_</span></span>
  
> <span data-ttu-id="e3f82-127">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e3f82-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="e3f82-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="e3f82-128">_binChg_</span></span>
  
> <span data-ttu-id="e3f82-129">[out]項目が移動された場合は、同期先項目のキーを変更します。</span><span class="sxs-lookup"><span data-stu-id="e3f82-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="e3f82-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="e3f82-130">_binPcl_</span></span>
  
> <span data-ttu-id="e3f82-131">[out]項目が移動された場合は、同期先項目の一覧を変更します。</span><span class="sxs-lookup"><span data-stu-id="e3f82-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="e3f82-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="e3f82-132">_skeyDst_</span></span>
  
> <span data-ttu-id="e3f82-133">[out]同期先項目の項目のソースのキーに移動されました。</span><span class="sxs-lookup"><span data-stu-id="e3f82-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="e3f82-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="e3f82-134">_pupmov_</span></span>
  
> <span data-ttu-id="e3f82-135">[out]アイテムのコピー先フォルダーの情報を移動するとします。</span><span class="sxs-lookup"><span data-stu-id="e3f82-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3f82-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3f82-136">See also</span></span>

- [<span data-ttu-id="e3f82-137">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="e3f82-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="e3f82-138">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="e3f82-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e3f82-139">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="e3f82-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="e3f82-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="e3f82-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="e3f82-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="e3f82-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="e3f82-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="e3f82-142">UPMOV</span></span>](upmov.md)

