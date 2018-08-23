---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c856dfd1d419fd7a4bf4f47852ffb69470f9281b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804067"
---
# <a name="sync"></a><span data-ttu-id="7c7ac-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="7c7ac-103">SYNC</span></span>

  
  
<span data-ttu-id="7c7ac-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c7ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c7ac-105">ローカル ストアとサーバ間の同期を開始するための情報です。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="7c7ac-106">この情報は、[状態を同期](synchronize-state.md)する際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7c7ac-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="7c7ac-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7c7ac-108">Members</span><span class="sxs-lookup"><span data-stu-id="7c7ac-108">Members</span></span>

 <span data-ttu-id="7c7ac-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7c7ac-109">_ulFlags_</span></span>
  
- <span data-ttu-id="7c7ac-110">[out]/[in] 同期中の動作を変更する次のフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="7c7ac-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="7c7ac-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="7c7ac-112">[in]クライアントのみのアップロードを実行します。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="7c7ac-113">Outlook は、ローカルで変更されたフォルダーのみを返します。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="7c7ac-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="7c7ac-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="7c7ac-115">[in]クライアントは、ダウンロードのみを実行しているが。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="7c7ac-116">Outlook は、フォルダーのアップロードのビットを消去しないでください。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="7c7ac-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="7c7ac-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="7c7ac-118">[in]クライアント同期するフォルダーの指定したセットで指定されたエントリ Id です。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="7c7ac-119">このフラグは、 **UPS_UPLOAD_ONLY**または**UPS_DNLOAD_ONLY**のいずれかのフラグを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="7c7ac-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="7c7ac-120">UPS_OK</span></span>
    
  - <span data-ttu-id="7c7ac-121">[out]同期が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="7c7ac-122">クライアントがこれをアップロードした後に設定、または完全な同期が完了するとします。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="7c7ac-123">にもかかわらず、クライアントのアップロードまたは完全に同期できます (アップロード、ダウンロード) フォルダーとアイテムは、レプリケーション API を使用してクライアントが同時にレプリケーションの方向が 1 つだけで*ulFlags*を指定-いずれかの**UPS_UPLOAD_ONLY**または**UPS_DNLOAD_ONLY**フラグです。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="7c7ac-124">クライアント、完全な同期の場合、 **UPS_UPLOAD_ONLY**フラグを使用してアップロードし、 **UPS_DNLOAD_ONLY**フラグを指定してダウンロードが最初に行われます。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="7c7ac-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="7c7ac-125">_pwzPath_</span></span>
  
- <span data-ttu-id="7c7ac-126">[out]ローカル ストアへのパス。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="7c7ac-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="7c7ac-127">_Reserved1_</span></span>
  
- <span data-ttu-id="7c7ac-128">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="7c7ac-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="7c7ac-129">_Reserved2_</span></span>
  
- <span data-ttu-id="7c7ac-130">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="7c7ac-131">*pel*</span><span class="sxs-lookup"><span data-stu-id="7c7ac-131">*pel*</span></span> 
  
- <span data-ttu-id="7c7ac-132">[in]これは、 **UPS_THESE_FOLDERS**が設定されている場合は、同期するフォルダーのエントリ Id の一覧です。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="7c7ac-133">**LPENTRYLIST**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="7c7ac-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="7c7ac-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="7c7ac-135">[in]これは、 **UPS_THESE_FOLDERS**が設定されている場合、 *pel*で対応するフォルダーのフォルダー オプションの配列です。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="7c7ac-136">これらのフォルダーのオプションは、各[フォルダーの状態をアップロード](upload-folder-state.md)する時に*pel*で表示されているフォルダーをアップロードするときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="7c7ac-137">フォルダー オプションの詳細については、 **[UPFLD](upfld.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c7ac-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7c7ac-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c7ac-138">See also</span></span>



[<span data-ttu-id="7c7ac-139">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="7c7ac-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7c7ac-140">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="7c7ac-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7c7ac-141">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="7c7ac-141">MAPI Constants</span></span>](mapi-constants.md)

