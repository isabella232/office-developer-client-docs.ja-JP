---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 34d6eb0653c3eb550bf03242a2c1b2acc3330a13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572292"
---
# <a name="upfld"></a><span data-ttu-id="c4c61-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="c4c61-103">UPFLD</span></span>

<span data-ttu-id="c4c61-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4c61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4c61-105">[フォルダーの状態をアップロード](upload-folder-state.md)する際にフォルダーをアップロードする方法の詳細については。</span><span class="sxs-lookup"><span data-stu-id="c4c61-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c4c61-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="c4c61-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="c4c61-107">Members</span><span class="sxs-lookup"><span data-stu-id="c4c61-107">Members</span></span>

<span data-ttu-id="c4c61-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c4c61-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="c4c61-109">[out]/[in]、uplaod の適切なアクションを決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="c4c61-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="c4c61-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="c4c61-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="c4c61-111">[out]フォルダーは、新しいです。</span><span class="sxs-lookup"><span data-stu-id="c4c61-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="c4c61-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="c4c61-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="c4c61-113">[out]フォルダーに移動されました。</span><span class="sxs-lookup"><span data-stu-id="c4c61-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="c4c61-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="c4c61-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="c4c61-115">[out]フォルダーのプロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="c4c61-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="c4c61-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="c4c61-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="c4c61-117">[out]フォルダーが削除されました。</span><span class="sxs-lookup"><span data-stu-id="c4c61-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="c4c61-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="c4c61-118">UPF_OK</span></span>
    
    - <span data-ttu-id="c4c61-119">[in]アップロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="c4c61-119">[in] Upload was successful.</span></span> <span data-ttu-id="c4c61-120">クライアントでは、フォルダー情報をサーバーにアップロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="c4c61-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="c4c61-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="c4c61-121">_pfld_</span></span>
  
> <span data-ttu-id="c4c61-122">[out]アップロードするフォルダーを開くオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="c4c61-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="c4c61-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="c4c61-123">_feid_</span></span>
  
> <span data-ttu-id="c4c61-124">[out]フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="c4c61-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4c61-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4c61-125">See also</span></span>

- [<span data-ttu-id="c4c61-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="c4c61-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="c4c61-127">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="c4c61-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="c4c61-128">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="c4c61-128">MAPI Constants</span></span>](mapi-constants.md)

