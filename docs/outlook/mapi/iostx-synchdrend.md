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
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591332"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="e7b47-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="e7b47-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="e7b47-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7b47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7b47-105">メッセージ ヘッダーの同期を終了します。</span><span class="sxs-lookup"><span data-stu-id="e7b47-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="e7b47-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e7b47-106">Parameters</span></span>

 <span data-ttu-id="e7b47-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="e7b47-107">_pprog_</span></span>
  
> <span data-ttu-id="e7b47-108">[in]同期のための**[IMAPIProgress](imapiprogressiunknown.md)** インタ フェースは、移動またはメッセージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="e7b47-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="e7b47-109">**LPMAPIPROGRESS**の型の定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7b47-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e7b47-110">注釈</span><span class="sxs-lookup"><span data-stu-id="e7b47-110">Remarks</span></span>

<span data-ttu-id="e7b47-111">**[IOSTX::SyncBeg](iostx-syncbeg.md)**、時に、ローカル ストアは、[メッセージ ヘッダーの状態をダウンロード](download-message-header-state.md)するを入力します。</span><span class="sxs-lookup"><span data-stu-id="e7b47-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="e7b47-112">クライアントは、( *pmsgFull*の**[HDRSYNC](hdrsync.md)** で) として、完全なメッセージ項目をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e7b47-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="e7b47-113">これが成功した場合は、クライアントも*ulFlags*の設定**HDRSYNC** **HSF_OK**とします。</span><span class="sxs-lookup"><span data-stu-id="e7b47-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="e7b47-114">**IOSTX::SyncHdrEnd**、時に、Outlook は**HDRSYNC**の結果をチェックし、ローカル メッセージのヘッダーを更新するのには、 **HDRSYNC**で*pprog*との情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="e7b47-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="e7b47-115">ローカル ストアは、 **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** の前の前に、の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="e7b47-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e7b47-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="e7b47-116">See also</span></span>



[<span data-ttu-id="e7b47-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e7b47-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="e7b47-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="e7b47-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="e7b47-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="e7b47-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="e7b47-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="e7b47-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="e7b47-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="e7b47-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="e7b47-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="e7b47-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="e7b47-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7b47-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="e7b47-124">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="e7b47-124">MAPI Constants</span></span>](mapi-constants.md)

