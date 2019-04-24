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
description: '最終更新日: 2012 年7月3日'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332187"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="6cef0-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="6cef0-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="6cef0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cef0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cef0-105">メッセージヘッダーの同期を終了します。</span><span class="sxs-lookup"><span data-stu-id="6cef0-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="6cef0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6cef0-106">Parameters</span></span>

 <span data-ttu-id="6cef0-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="6cef0-107">_pprog_</span></span>
  
> <span data-ttu-id="6cef0-108">順番移動またはコピーされたメッセージを同期するための**[imapiprogress](imapiprogressiunknown.md)** インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="6cef0-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="6cef0-109">**LPMAPIPROGRESS**の型定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6cef0-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6cef0-110">解説</span><span class="sxs-lookup"><span data-stu-id="6cef0-110">Remarks</span></span>

<span data-ttu-id="6cef0-111">**[iostx:: SyncBeg](iostx-syncbeg.md)** の場合、ローカルストアは[ダウンロードメッセージヘッダーの状態](download-message-header-state.md)を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cef0-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="6cef0-112">クライアントは、完全なメッセージアイテム ( **[HDRSYNC](hdrsync.md)** では*pmsgfull* ) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6cef0-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="6cef0-113">この処理が成功した場合、クライアントは**HSF_OK**として**HDRSYNC**の*ulflags*も設定します。</span><span class="sxs-lookup"><span data-stu-id="6cef0-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="6cef0-114">**iostx:: SyncHdrEnd**の場合、Outlook は**HDRSYNC**の結果をチェックし、 *pprog*と**HDRSYNC**内の情報を使用して、ローカルメッセージヘッダーを更新します。</span><span class="sxs-lookup"><span data-stu-id="6cef0-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="6cef0-115">ローカルストアは、前の**[iostx:: SyncHdrBeg](iostx-synchdrbeg.md)** の前の状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="6cef0-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6cef0-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="6cef0-116">See also</span></span>



[<span data-ttu-id="6cef0-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6cef0-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="6cef0-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="6cef0-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="6cef0-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="6cef0-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="6cef0-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="6cef0-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="6cef0-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="6cef0-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="6cef0-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="6cef0-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="6cef0-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6cef0-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="6cef0-124">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="6cef0-124">MAPI Constants</span></span>](mapi-constants.md)

