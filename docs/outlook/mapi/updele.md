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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424883"
---
# <a name="updele"></a><span data-ttu-id="1d38a-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="1d38a-103">UPDELE</span></span>

<span data-ttu-id="1d38a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d38a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d38a-105">ローカル ストアで削除されたアイテムの拡張情報。</span><span class="sxs-lookup"><span data-stu-id="1d38a-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="1d38a-106">この情報は、アップロードの削除状態 [の間に使用されます](upload-delete-status-state.md)。</span><span class="sxs-lookup"><span data-stu-id="1d38a-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1d38a-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1d38a-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="1d38a-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="1d38a-108">Members</span></span>

<span data-ttu-id="1d38a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1d38a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1d38a-110">[out]/[in] アップロード時の適切な動作を判断するフラグ。</span><span class="sxs-lookup"><span data-stu-id="1d38a-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="1d38a-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="1d38a-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="1d38a-112">[out]アイテムが関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="1d38a-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="1d38a-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="1d38a-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="1d38a-114">[out]アイテムが移動されました。</span><span class="sxs-lookup"><span data-stu-id="1d38a-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="1d38a-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="1d38a-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="1d38a-116">[in]アップロード成功しました。</span><span class="sxs-lookup"><span data-stu-id="1d38a-116">[in] Upload was successful.</span></span> <span data-ttu-id="1d38a-117">クライアントは、サーバーに情報をアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="1d38a-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="1d38a-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="1d38a-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="1d38a-119">[in]アイテムが正常に移動されました。</span><span class="sxs-lookup"><span data-stu-id="1d38a-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="1d38a-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="1d38a-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="1d38a-121">[in]変更済みとしてソース アイテムをマークします。</span><span class="sxs-lookup"><span data-stu-id="1d38a-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="1d38a-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="1d38a-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="1d38a-123">[in]アップロードの状態を今すぐコミットします (エントリ 0)。</span><span class="sxs-lookup"><span data-stu-id="1d38a-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="1d38a-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="1d38a-124">_skey_</span></span>
  
> <span data-ttu-id="1d38a-125">[out]アイテムのソース キー。</span><span class="sxs-lookup"><span data-stu-id="1d38a-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="1d38a-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="1d38a-126">_dwReserved_</span></span>
  
> <span data-ttu-id="1d38a-127">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1d38a-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="1d38a-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="1d38a-128">_binChg_</span></span>
  
> <span data-ttu-id="1d38a-129">[out]アイテムが移動されている場合は、移動先アイテムのキーを変更します。</span><span class="sxs-lookup"><span data-stu-id="1d38a-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="1d38a-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="1d38a-130">_binPcl_</span></span>
  
> <span data-ttu-id="1d38a-131">[out]アイテムが移動されている場合は、移動先アイテムのリストを変更します。</span><span class="sxs-lookup"><span data-stu-id="1d38a-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="1d38a-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="1d38a-132">_skeyDst_</span></span>
  
> <span data-ttu-id="1d38a-133">[out]アイテムが移動されている場合の移動先アイテムのソース キー。</span><span class="sxs-lookup"><span data-stu-id="1d38a-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="1d38a-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="1d38a-134">_pupmov_</span></span>
  
> <span data-ttu-id="1d38a-135">[out]アイテムが移動された場合の移動先フォルダー情報。</span><span class="sxs-lookup"><span data-stu-id="1d38a-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d38a-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d38a-136">See also</span></span>

- [<span data-ttu-id="1d38a-137">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="1d38a-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="1d38a-138">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="1d38a-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1d38a-139">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="1d38a-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="1d38a-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="1d38a-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="1d38a-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="1d38a-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="1d38a-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="1d38a-142">UPMOV</span></span>](upmov.md)

