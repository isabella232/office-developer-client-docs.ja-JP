---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349596"
---
# <a name="sync"></a><span data-ttu-id="522e1-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="522e1-103">SYNC</span></span>

  
  
<span data-ttu-id="522e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="522e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="522e1-105">ローカルストアとサーバーの間の同期を開始するための情報。</span><span class="sxs-lookup"><span data-stu-id="522e1-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="522e1-106">この情報は、[同期状態](synchronize-state.md)の間に使用されます。</span><span class="sxs-lookup"><span data-stu-id="522e1-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="522e1-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="522e1-107">Quick info</span></span>

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a><span data-ttu-id="522e1-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="522e1-108">Members</span></span>

 <span data-ttu-id="522e1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="522e1-109">_ulFlags_</span></span>
  
- <span data-ttu-id="522e1-110">[out]/[in] 同期中の動作を変更する次のフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="522e1-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="522e1-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="522e1-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="522e1-112">順番クライアントはアップロードのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="522e1-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="522e1-113">Outlook は、ローカルで変更されたフォルダーのみを返します。</span><span class="sxs-lookup"><span data-stu-id="522e1-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="522e1-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="522e1-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="522e1-115">順番クライアントはダウンロードのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="522e1-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="522e1-116">Outlook では、フォルダーのアップロードビットをクリアすることはできません。</span><span class="sxs-lookup"><span data-stu-id="522e1-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="522e1-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="522e1-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="522e1-118">順番クライアントは、指定されたフォルダーのセットと指定されたエントリ id を同期します。</span><span class="sxs-lookup"><span data-stu-id="522e1-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="522e1-119">このフラグは、 **UPS_UPLOAD_ONLY**または**UPS_DNLOAD_ONLY**のいずれかのフラグと組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="522e1-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="522e1-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="522e1-120">UPS_OK</span></span>
    
  - <span data-ttu-id="522e1-121">読み上げ同期に成功しました。</span><span class="sxs-lookup"><span data-stu-id="522e1-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="522e1-122">クライアントは、アップロード後または完全同期の完了後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="522e1-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="522e1-123">クライアントは、レプリケーション API を使用してフォルダーとアイテムをアップロードまたは完全に同期 (アップロードしてからダウンロード) することができますが、クライアントは一度にレプリケーションの方向が1つだけの*ulflags*を指定します ( **UPS_UPLOAD_ONLY**または**UPS_DNLOAD_ONLY**フラグ。</span><span class="sxs-lookup"><span data-stu-id="522e1-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="522e1-124">完全同期の場合、クライアントはまず**UPS_UPLOAD_ONLY**フラグを使用してアップロードを行い、 **UPS_DNLOAD_ONLY**フラグを使用してダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="522e1-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="522e1-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="522e1-125">_pwzPath_</span></span>
  
- <span data-ttu-id="522e1-126">読み上げローカルストアへのパス。</span><span class="sxs-lookup"><span data-stu-id="522e1-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="522e1-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="522e1-127">_Reserved1_</span></span>
  
- <span data-ttu-id="522e1-128">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="522e1-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="522e1-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="522e1-129">_Reserved2_</span></span>
  
- <span data-ttu-id="522e1-130">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="522e1-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="522e1-131">*bpel*</span><span class="sxs-lookup"><span data-stu-id="522e1-131">*pel*</span></span> 
  
- <span data-ttu-id="522e1-132">順番これは、 **UPS_THESE_FOLDERS**が設定されている場合に同期するフォルダーのエントリ id の一覧です。</span><span class="sxs-lookup"><span data-stu-id="522e1-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="522e1-133">**lmapidefs.h trylist**の型定義については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="522e1-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="522e1-134">_/オプション_</span><span class="sxs-lookup"><span data-stu-id="522e1-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="522e1-135">順番**UPS_THESE_FOLDERS**が設定されている場合、 *pel*内の対応するフォルダーのフォルダオプションの配列です。</span><span class="sxs-lookup"><span data-stu-id="522e1-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="522e1-136">これらのフォルダーオプションは、「 [upload フォルダーの状態](upload-folder-state.md)」で*pel*にリストされている各フォルダーをアップロードするときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="522e1-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="522e1-137">フォルダーオプションの詳細については、「 **[UPFLD](upfld.md)**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="522e1-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="522e1-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="522e1-138">See also</span></span>



[<span data-ttu-id="522e1-139">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="522e1-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="522e1-140">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="522e1-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="522e1-141">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="522e1-141">MAPI Constants</span></span>](mapi-constants.md)

