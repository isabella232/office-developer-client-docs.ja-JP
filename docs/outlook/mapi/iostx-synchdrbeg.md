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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a5c754a209a3e1bce8888851b88e116f92920eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801088"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="5e17d-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="5e17d-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="5e17d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e17d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e17d-105">メッセージ ヘッダーの同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="5e17d-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="5e17d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5e17d-106">Parameters</span></span>

 <span data-ttu-id="5e17d-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="5e17d-107">_cbeid_</span></span>
  
> <span data-ttu-id="5e17d-108">[in]メッセージのエントリ ID 内のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="5e17d-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="5e17d-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="5e17d-109">_lpeid_</span></span>
  
> <span data-ttu-id="5e17d-110">[in]メッセージのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="5e17d-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="5e17d-111">_ppv_</span><span class="sxs-lookup"><span data-stu-id="5e17d-111">_ppv_</span></span>
  
>  <span data-ttu-id="5e17d-112">[内] と [出力] メッセージ ヘッダーの**[HDRSYNC](hdrsync.md)** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5e17d-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5e17d-113">備考</span><span class="sxs-lookup"><span data-stu-id="5e17d-113">Remarks</span></span>

<span data-ttu-id="5e17d-114">**IOSTX::SyncHdrBeg**、時に、ローカルは、[メッセージ ヘッダーの状態をダウンロードする](download-message-header-state.md)に効果を格納します。</span><span class="sxs-lookup"><span data-stu-id="5e17d-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="5e17d-115">Outlook は、クライアントがストアに格納され、親フォルダーのメッセージのヘッダーの現在の表現を**HDRSYNC**構造体を初期化します。</span><span class="sxs-lookup"><span data-stu-id="5e17d-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="5e17d-116">クライアントは、( *pmsgFull*の**HDRSYNC**で) として、完全なメッセージ項目をダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e17d-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="5e17d-117">これが成功した場合、クライアントも*ulFlags*の設定**HDRSYNC** **HSF_OK**とします。</span><span class="sxs-lookup"><span data-stu-id="5e17d-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="5e17d-118">**[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**、時に、Outlook は**HDRSYNC**の結果をチェックし、 **HDRSYNC**で情報を使用して、ローカルのメッセージ ヘッダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="5e17d-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e17d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e17d-119">See also</span></span>



[<span data-ttu-id="5e17d-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5e17d-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="5e17d-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="5e17d-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="5e17d-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="5e17d-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="5e17d-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="5e17d-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="5e17d-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="5e17d-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="5e17d-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="5e17d-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="5e17d-126">IOSTX: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e17d-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="5e17d-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="5e17d-127">MAPI Constants</span></span>](mapi-constants.md)

