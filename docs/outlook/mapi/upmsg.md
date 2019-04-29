---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427270"
---
# <a name="upmsg"></a><span data-ttu-id="70737-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="70737-103">UPMSG</span></span>

<span data-ttu-id="70737-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70737-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70737-105">[アップロードメッセージの状態](upload-message-state.md)中に Outlook アイテムをアップロードするための情報。</span><span class="sxs-lookup"><span data-stu-id="70737-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="70737-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="70737-106">Quick info</span></span>

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a><span data-ttu-id="70737-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="70737-107">Members</span></span>

 <span data-ttu-id="70737-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70737-108">_ulFlags_</span></span>
  
> <span data-ttu-id="70737-109">[out]/[in] フラグを指定して、アップロード中の適切な動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="70737-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="70737-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="70737-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="70737-111">読み上げ項目が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="70737-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="70737-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="70737-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="70737-113">読み上げ新しいアイテム。</span><span class="sxs-lookup"><span data-stu-id="70737-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="70737-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="70737-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="70737-115">読み上げアイテムはここに移動されました。</span><span class="sxs-lookup"><span data-stu-id="70737-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="70737-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="70737-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="70737-117">読み上げアイテムのプロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="70737-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="70737-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="70737-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="70737-119">読み上げアイテムはメッセージヘッダーです。</span><span class="sxs-lookup"><span data-stu-id="70737-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="70737-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="70737-120">UPM_OK</span></span>
    
    - <span data-ttu-id="70737-121">順番アップロードに成功しました。</span><span class="sxs-lookup"><span data-stu-id="70737-121">[in] Upload was successful.</span></span> <span data-ttu-id="70737-122">クライアントは、情報をサーバーにアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="70737-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="70737-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="70737-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="70737-124">順番アイテムは正常に移動されました。</span><span class="sxs-lookup"><span data-stu-id="70737-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="70737-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="70737-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="70737-126">順番今すぐアップロードの状態をコミットします。</span><span class="sxs-lookup"><span data-stu-id="70737-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="70737-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="70737-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="70737-128">順番今すぐアイテムを削除します。</span><span class="sxs-lookup"><span data-stu-id="70737-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="70737-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="70737-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="70737-130">順番アイテムへの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="70737-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="70737-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="70737-131">_pmsg_</span></span>
  
> <span data-ttu-id="70737-132">読み上げアイテムオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="70737-132">[out] Open item object.</span></span> <span data-ttu-id="70737-133">**lpmessage**の種類の定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70737-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="70737-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="70737-134">_meid_</span></span>
  
> <span data-ttu-id="70737-135">読み上げアイテムのエントリ ID。</span><span class="sxs-lookup"><span data-stu-id="70737-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="70737-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="70737-136">_binReserved1_</span></span>
  
> <span data-ttu-id="70737-137">順番このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="70737-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="70737-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="70737-138">_binReserved2_</span></span>
  
> <span data-ttu-id="70737-139">順番このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="70737-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="70737-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="70737-140">_feid_</span></span>
  
> <span data-ttu-id="70737-141">読み上げアイテムが移動された場合は、ソースフォルダーのエントリ ID。</span><span class="sxs-lookup"><span data-stu-id="70737-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="70737-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="70737-142">_binChg_</span></span>
  
> <span data-ttu-id="70737-143">読み上げアイテムが移動された場合は、コピー先アイテムのキーを変更します。</span><span class="sxs-lookup"><span data-stu-id="70737-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="70737-144">**sbinary**の型定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70737-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="70737-145">_binpcl_</span><span class="sxs-lookup"><span data-stu-id="70737-145">_binPcl_</span></span>
  
> <span data-ttu-id="70737-146">読み上げアイテムが移動された場合は、コピー先アイテムのリストを変更します。</span><span class="sxs-lookup"><span data-stu-id="70737-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="70737-147">**sbinary**の型定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="70737-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="70737-148">_skeysrc_</span><span class="sxs-lookup"><span data-stu-id="70737-148">_skeySrc_</span></span>
  
> <span data-ttu-id="70737-149">読み上げアイテムが移動された場合は、ソースアイテムのソースキー。</span><span class="sxs-lookup"><span data-stu-id="70737-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70737-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="70737-150">See also</span></span>

- [<span data-ttu-id="70737-151">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="70737-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="70737-152">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="70737-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="70737-153">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="70737-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="70737-154">FEID</span><span class="sxs-lookup"><span data-stu-id="70737-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="70737-155">MEID</span><span class="sxs-lookup"><span data-stu-id="70737-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="70737-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="70737-156">SKEY</span></span>](skey.md)

