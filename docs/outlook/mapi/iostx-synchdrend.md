---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: ee68052f330bf3239cd12139ffbd77f5a180f6cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801090"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="9e0b4-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="9e0b4-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="9e0b4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e0b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e0b4-105">メッセージ ヘッダーの同期を終了します。</span><span class="sxs-lookup"><span data-stu-id="9e0b4-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="9e0b4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9e0b4-106">Parameters</span></span>

 <span data-ttu-id="9e0b4-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="9e0b4-107">_pprog_</span></span>
  
> <span data-ttu-id="9e0b4-108">[in]同期のための**[IMAPIProgress](imapiprogressiunknown.md)** インタ フェースは、移動またはメッセージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="9e0b4-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="9e0b4-109">**LPMAPIPROGRESS**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9e0b4-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e0b4-110">注釈</span><span class="sxs-lookup"><span data-stu-id="9e0b4-110">Remarks</span></span>

<span data-ttu-id="9e0b4-111">**[IOSTX::SyncBeg](iostx-syncbeg.md)**、時に、ローカル ストアは、[メッセージ ヘッダーの状態をダウンロード](download-message-header-state.md)するを入力します。</span><span class="sxs-lookup"><span data-stu-id="9e0b4-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="9e0b4-112">クライアントは、( *pmsgFull*の**[HDRSYNC](hdrsync.md)** で) として、完全なメッセージ項目をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9e0b4-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="9e0b4-113">これが成功した場合は、クライアントも*ulFlags*の設定**HDRSYNC** **HSF_OK**とします。</span><span class="sxs-lookup"><span data-stu-id="9e0b4-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="9e0b4-114">**IOSTX::SyncHdrEnd**、時に、Outlook は**HDRSYNC**の結果をチェックし、ローカル メッセージのヘッダーを更新するのには、 **HDRSYNC**で*pprog*との情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="9e0b4-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="9e0b4-115">ローカル ストアは、 **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** の前の前に、の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="9e0b4-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e0b4-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e0b4-116">See also</span></span>



[<span data-ttu-id="9e0b4-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9e0b4-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="9e0b4-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="9e0b4-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="9e0b4-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="9e0b4-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="9e0b4-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="9e0b4-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="9e0b4-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="9e0b4-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="9e0b4-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="9e0b4-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="9e0b4-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e0b4-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="9e0b4-124">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="9e0b4-124">MAPI Constants</span></span>](mapi-constants.md)

