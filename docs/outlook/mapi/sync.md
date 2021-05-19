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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433809"
---
# <a name="sync"></a><span data-ttu-id="0a514-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="0a514-103">SYNC</span></span>

  
  
<span data-ttu-id="0a514-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a514-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a514-105">ローカル ストアとサーバー間の同期を開始する情報。</span><span class="sxs-lookup"><span data-stu-id="0a514-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="0a514-106">この情報は、同期状態の間 [に使用されます](synchronize-state.md)。</span><span class="sxs-lookup"><span data-stu-id="0a514-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0a514-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0a514-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="0a514-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="0a514-108">Members</span></span>

 <span data-ttu-id="0a514-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0a514-109">_ulFlags_</span></span>
  
- <span data-ttu-id="0a514-110">[out]/[in] 同期中の動作を変更する次のフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0a514-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="0a514-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="0a514-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="0a514-112">[in]クライアントはアップロードのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="0a514-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="0a514-113">Outlook変更されたフォルダーのみを返します。</span><span class="sxs-lookup"><span data-stu-id="0a514-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="0a514-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="0a514-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="0a514-115">[in]クライアントはダウンロードのみを実行します。</span><span class="sxs-lookup"><span data-stu-id="0a514-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="0a514-116">Outlookのアップロード ビットをクリアしない必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a514-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="0a514-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="0a514-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="0a514-118">[in]クライアントは、指定された一連のフォルダーを、指定されたエントリ ID と同期します。</span><span class="sxs-lookup"><span data-stu-id="0a514-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="0a514-119">このフラグは、UPS_UPLOAD_ONLY **またはUPS_DNLOAD_ONLY\*\*\*\*できます。**</span><span class="sxs-lookup"><span data-stu-id="0a514-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="0a514-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="0a514-120">UPS_OK</span></span>
    
  - <span data-ttu-id="0a514-121">[out]同期が成功しました。</span><span class="sxs-lookup"><span data-stu-id="0a514-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="0a514-122">クライアントは、アップロード後、または完全同期が完了した後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="0a514-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="0a514-123">クライアントは、レプリケーション API とフォルダーとアイテムをアップロードまたは完全に同期 (アップロードしてからダウンロード) することもできますが、クライアントは **、UPS_UPLOAD_ONLY** フラグまたは UPS_DNLOAD_ONLY フラグのいずれかである一度にレプリケーションの方向が 1 つのみ *ulFlags* **を指定** します。</span><span class="sxs-lookup"><span data-stu-id="0a514-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="0a514-124">完全同期の場合、クライアントは最初に UPS_UPLOAD_ONLY フラグを使用してアップロードを行い、次に UPS_DNLOAD_ONLY フラグ **をUPS_DNLOAD_ONLY** します。</span><span class="sxs-lookup"><span data-stu-id="0a514-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="0a514-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="0a514-125">_pwzPath_</span></span>
  
- <span data-ttu-id="0a514-126">[out]ローカル ストアへのパス。</span><span class="sxs-lookup"><span data-stu-id="0a514-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="0a514-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="0a514-127">_Reserved1_</span></span>
  
- <span data-ttu-id="0a514-128">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0a514-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="0a514-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="0a514-129">_Reserved2_</span></span>
  
- <span data-ttu-id="0a514-130">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0a514-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="0a514-131">*pel*</span><span class="sxs-lookup"><span data-stu-id="0a514-131">*pel*</span></span> 
  
- <span data-ttu-id="0a514-132">[in]これは、フォルダーが設定されている場合に同期するフォルダー **UPS_THESE_FOLDERS** 一覧です。</span><span class="sxs-lookup"><span data-stu-id="0a514-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="0a514-133">**LPENTRYLIST** の型定義については、mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a514-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="0a514-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="0a514-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="0a514-135">[in]これは、プロパティが設定されている場合、pel 内の **対応するフォルダー UPS_THESE_FOLDERS** 配列です。</span><span class="sxs-lookup"><span data-stu-id="0a514-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="0a514-136">これらのフォルダー オプションは、アップロード フォルダーの状態の間に  *pel*  にリストされている各フォルダーをアップロード [するときに使用されます](upload-folder-state.md)。</span><span class="sxs-lookup"><span data-stu-id="0a514-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="0a514-137">フォルダー オプションの詳細については **[、「UPFLD」を参照してください](upfld.md)**。</span><span class="sxs-lookup"><span data-stu-id="0a514-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0a514-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a514-138">See also</span></span>



[<span data-ttu-id="0a514-139">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="0a514-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="0a514-140">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="0a514-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="0a514-141">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="0a514-141">MAPI Constants</span></span>](mapi-constants.md)

