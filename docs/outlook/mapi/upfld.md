---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431359"
---
# <a name="upfld"></a><span data-ttu-id="01d1d-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="01d1d-103">UPFLD</span></span>

<span data-ttu-id="01d1d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01d1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01d1d-105">アップロード フォルダーの状態中にフォルダーを [アップロードする場合の情報](upload-folder-state.md)です。</span><span class="sxs-lookup"><span data-stu-id="01d1d-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="01d1d-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="01d1d-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="01d1d-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="01d1d-107">Members</span></span>

<span data-ttu-id="01d1d-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="01d1d-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="01d1d-109">[out]/[in] uplaod に対する適切なアクションを決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="01d1d-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="01d1d-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="01d1d-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="01d1d-111">[out]フォルダーが新しい。</span><span class="sxs-lookup"><span data-stu-id="01d1d-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="01d1d-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="01d1d-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="01d1d-113">[out]フォルダーが移動されました。</span><span class="sxs-lookup"><span data-stu-id="01d1d-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="01d1d-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="01d1d-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="01d1d-115">[out]フォルダーのプロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="01d1d-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="01d1d-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="01d1d-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="01d1d-117">[out]フォルダーが削除されました。</span><span class="sxs-lookup"><span data-stu-id="01d1d-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="01d1d-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="01d1d-118">UPF_OK</span></span>
    
    - <span data-ttu-id="01d1d-119">[in]アップロード成功しました。</span><span class="sxs-lookup"><span data-stu-id="01d1d-119">[in] Upload was successful.</span></span> <span data-ttu-id="01d1d-120">クライアントは、フォルダー情報をサーバーにアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="01d1d-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="01d1d-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="01d1d-121">_pfld_</span></span>
  
> <span data-ttu-id="01d1d-122">[out]アップロードする開いているフォルダー オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="01d1d-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="01d1d-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="01d1d-123">_feid_</span></span>
  
> <span data-ttu-id="01d1d-124">[out] フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="01d1d-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01d1d-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="01d1d-125">See also</span></span>

- [<span data-ttu-id="01d1d-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="01d1d-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="01d1d-127">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="01d1d-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="01d1d-128">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="01d1d-128">MAPI Constants</span></span>](mapi-constants.md)

