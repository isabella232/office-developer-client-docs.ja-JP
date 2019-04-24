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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360481"
---
# <a name="upfld"></a><span data-ttu-id="5f034-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="5f034-103">UPFLD</span></span>

<span data-ttu-id="5f034-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f034-105">[アップロードフォルダーの状態](upload-folder-state.md)中にフォルダーをアップロードするための情報。</span><span class="sxs-lookup"><span data-stu-id="5f034-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5f034-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5f034-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="5f034-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="5f034-107">Members</span></span>

<span data-ttu-id="5f034-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5f034-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="5f034-109">[out]/[in] フラグを使用して、uて od の適切なアクションを特定します。</span><span class="sxs-lookup"><span data-stu-id="5f034-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="5f034-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="5f034-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="5f034-111">読み上げFolder は新規です。</span><span class="sxs-lookup"><span data-stu-id="5f034-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="5f034-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="5f034-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="5f034-113">読み上げフォルダーが移動されました。</span><span class="sxs-lookup"><span data-stu-id="5f034-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="5f034-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="5f034-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="5f034-115">読み上げフォルダーのプロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="5f034-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="5f034-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="5f034-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="5f034-117">読み上げフォルダーが削除されました。</span><span class="sxs-lookup"><span data-stu-id="5f034-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="5f034-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="5f034-118">UPF_OK</span></span>
    
    - <span data-ttu-id="5f034-119">順番アップロードに成功しました。</span><span class="sxs-lookup"><span data-stu-id="5f034-119">[in] Upload was successful.</span></span> <span data-ttu-id="5f034-120">サーバーにフォルダー情報をアップロードした後、クライアントはこの設定を行います。</span><span class="sxs-lookup"><span data-stu-id="5f034-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="5f034-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="5f034-121">_pfld_</span></span>
  
> <span data-ttu-id="5f034-122">読み上げアップロードする開いている folder オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5f034-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="5f034-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="5f034-123">_feid_</span></span>
  
> <span data-ttu-id="5f034-124">[out] フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="5f034-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f034-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f034-125">See also</span></span>

- [<span data-ttu-id="5f034-126">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="5f034-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="5f034-127">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="5f034-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="5f034-128">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="5f034-128">MAPI Constants</span></span>](mapi-constants.md)

