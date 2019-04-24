---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317158"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="e5d61-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="e5d61-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="e5d61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5d61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5d61-105">メッセージヘッダーの同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="e5d61-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="e5d61-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e5d61-106">Parameters</span></span>

 <span data-ttu-id="e5d61-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="e5d61-107">_cbeid_</span></span>
  
> <span data-ttu-id="e5d61-108">順番メッセージのエントリ ID のバイト数。</span><span class="sxs-lookup"><span data-stu-id="e5d61-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="e5d61-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="e5d61-109">_lpeid_</span></span>
  
> <span data-ttu-id="e5d61-110">順番メッセージのエントリ ID。</span><span class="sxs-lookup"><span data-stu-id="e5d61-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="e5d61-111">_ppv_</span><span class="sxs-lookup"><span data-stu-id="e5d61-111">_ppv_</span></span>
  
>  <span data-ttu-id="e5d61-112">[in]/[out] メッセージヘッダーの**[HDRSYNC](hdrsync.md)** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e5d61-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e5d61-113">解説</span><span class="sxs-lookup"><span data-stu-id="e5d61-113">Remarks</span></span>

<span data-ttu-id="e5d61-114">**iostx:: SyncHdrBeg**では、ローカルストアは、[メッセージヘッダーのダウンロード状態](download-message-header-state.md)に移行します。</span><span class="sxs-lookup"><span data-stu-id="e5d61-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="e5d61-115">Outlook は、ストア内の現在のメッセージヘッダーと親フォルダーを使用して、クライアントの**HDRSYNC**構造を初期化します。</span><span class="sxs-lookup"><span data-stu-id="e5d61-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="e5d61-116">クライアントは、完全なメッセージアイテム ( **HDRSYNC**では*pmsgfull*として) をダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5d61-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="e5d61-117">これが成功した場合、クライアントは**HSF_OK**として**HDRSYNC**の*ulflags*も設定します。</span><span class="sxs-lookup"><span data-stu-id="e5d61-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="e5d61-118">**[iostx:: SyncHdrEnd](iostx-synchdrend.md)** では、Outlook が**HDRSYNC**で結果をチェックし、 **HDRSYNC**の情報を使用してローカルメッセージヘッダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="e5d61-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5d61-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5d61-119">See also</span></span>



[<span data-ttu-id="e5d61-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e5d61-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="e5d61-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="e5d61-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="e5d61-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="e5d61-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="e5d61-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="e5d61-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="e5d61-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="e5d61-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="e5d61-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="e5d61-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="e5d61-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5d61-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="e5d61-127">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="e5d61-127">MAPI Constants</span></span>](mapi-constants.md)

