---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804193"
---
# <a name="upmsg"></a><span data-ttu-id="f58ed-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="f58ed-103">UPMSG</span></span>

<span data-ttu-id="f58ed-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f58ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f58ed-105">[メッセージの状態をアップロード](upload-message-state.md)する際に Outlook アイテムをアップロードする方法の詳細については。</span><span class="sxs-lookup"><span data-stu-id="f58ed-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f58ed-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f58ed-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="f58ed-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="f58ed-107">Members</span></span>

 <span data-ttu-id="f58ed-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f58ed-108">_ulFlags_</span></span>
  
> <span data-ttu-id="f58ed-109">[out]/[in] アップロード中に、適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="f58ed-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="f58ed-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="f58ed-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="f58ed-111">[out]項目に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="f58ed-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="f58ed-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="f58ed-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="f58ed-113">[out]新しい項目。</span><span class="sxs-lookup"><span data-stu-id="f58ed-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="f58ed-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="f58ed-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="f58ed-115">[out]項目をここに移動しました。</span><span class="sxs-lookup"><span data-stu-id="f58ed-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="f58ed-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="f58ed-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="f58ed-117">[out]アイテムのプロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="f58ed-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="f58ed-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="f58ed-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="f58ed-119">[out]メッセージ ヘッダーの項目です。</span><span class="sxs-lookup"><span data-stu-id="f58ed-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="f58ed-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="f58ed-120">UPM_OK</span></span>
    
    - <span data-ttu-id="f58ed-121">[in]アップロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="f58ed-121">[in] Upload was successful.</span></span> <span data-ttu-id="f58ed-122">クライアントでは、情報をサーバーにアップロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="f58ed-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="f58ed-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="f58ed-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="f58ed-124">[in]項目が正常に移動されました。</span><span class="sxs-lookup"><span data-stu-id="f58ed-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="f58ed-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="f58ed-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="f58ed-126">[in]今すぐアップロードの状態を反映します。</span><span class="sxs-lookup"><span data-stu-id="f58ed-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="f58ed-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="f58ed-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="f58ed-128">[in]アイテムを今すぐ削除します。</span><span class="sxs-lookup"><span data-stu-id="f58ed-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="f58ed-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="f58ed-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="f58ed-130">[in]アイテムに変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="f58ed-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="f58ed-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="f58ed-131">_pmsg_</span></span>
  
> <span data-ttu-id="f58ed-132">[out]アイテム オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="f58ed-132">[out] Open item object.</span></span> <span data-ttu-id="f58ed-133">**LPMESSAGE**の型定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f58ed-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="f58ed-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="f58ed-134">_meid_</span></span>
  
> <span data-ttu-id="f58ed-135">[out]アイテムのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="f58ed-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="f58ed-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="f58ed-136">_binReserved1_</span></span>
  
> <span data-ttu-id="f58ed-137">[in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f58ed-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="f58ed-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="f58ed-138">_binReserved2_</span></span>
  
> <span data-ttu-id="f58ed-139">[in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f58ed-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="f58ed-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="f58ed-140">_feid_</span></span>
  
> <span data-ttu-id="f58ed-141">[out]項目が移動された場合、元のフォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="f58ed-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="f58ed-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="f58ed-142">_binChg_</span></span>
  
> <span data-ttu-id="f58ed-143">[out]項目が移動された場合は、同期先の項目のキーを変更します。</span><span class="sxs-lookup"><span data-stu-id="f58ed-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="f58ed-144">**SBinary**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f58ed-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="f58ed-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="f58ed-145">_binPcl_</span></span>
  
> <span data-ttu-id="f58ed-146">[out]項目が移動された場合は、同期先の項目の一覧を変更します。</span><span class="sxs-lookup"><span data-stu-id="f58ed-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="f58ed-147">**SBinary**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f58ed-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="f58ed-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="f58ed-148">_skeySrc_</span></span>
  
> <span data-ttu-id="f58ed-149">[out]項目が移動された場合、元の項目のソースのキーです。</span><span class="sxs-lookup"><span data-stu-id="f58ed-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f58ed-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="f58ed-150">See also</span></span>

- [<span data-ttu-id="f58ed-151">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="f58ed-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="f58ed-152">レプリケーション状態マシンについて</span><span class="sxs-lookup"><span data-stu-id="f58ed-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="f58ed-153">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="f58ed-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="f58ed-154">FEID</span><span class="sxs-lookup"><span data-stu-id="f58ed-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="f58ed-155">MEID</span><span class="sxs-lookup"><span data-stu-id="f58ed-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="f58ed-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="f58ed-156">SKEY</span></span>](skey.md)

