---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434145"
---
# <a name="upreade"></a><span data-ttu-id="4b04e-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="4b04e-103">UPREADE</span></span>

<span data-ttu-id="4b04e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b04e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b04e-105">[[読み取り状態のアップロード] 状態](upload-read-status-state.md)の間にアイテムの読み取り状態をアップロードするための拡張情報。</span><span class="sxs-lookup"><span data-stu-id="4b04e-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4b04e-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="4b04e-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="4b04e-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="4b04e-107">Members</span></span>

<span data-ttu-id="4b04e-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b04e-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="4b04e-109">[out]/[in] フラグを指定して、アップロード中の適切な動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="4b04e-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="4b04e-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="4b04e-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="4b04e-111">読み上げ項目は表示されません。</span><span class="sxs-lookup"><span data-stu-id="4b04e-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="4b04e-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="4b04e-112">UPR_READ</span></span>
    
    - <span data-ttu-id="4b04e-113">読み上げアイテムの読み取り状態が変更されました。</span><span class="sxs-lookup"><span data-stu-id="4b04e-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="4b04e-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="4b04e-114">UPR_OK</span></span>
    
    - <span data-ttu-id="4b04e-115">順番アップロードに成功しました。</span><span class="sxs-lookup"><span data-stu-id="4b04e-115">[in] Upload was successful.</span></span> <span data-ttu-id="4b04e-116">クライアントは、情報をサーバーにアップロードした後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="4b04e-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="4b04e-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="4b04e-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="4b04e-118">順番この時点でアイテムの読み取り状態をアップロードします。これは、1つ以上のアイテムをバッチ処理するために、[アップロードテーブルの状態](upload-table-state.md)が終了するのを待つ代わりに行います。</span><span class="sxs-lookup"><span data-stu-id="4b04e-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="4b04e-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="4b04e-119">_skey_</span></span>
  
> <span data-ttu-id="4b04e-120">読み上げアイテムのソースキー。</span><span class="sxs-lookup"><span data-stu-id="4b04e-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b04e-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b04e-121">See also</span></span>

- [<span data-ttu-id="4b04e-122">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="4b04e-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="4b04e-123">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="4b04e-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="4b04e-124">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="4b04e-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="4b04e-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="4b04e-125">UPREAD</span></span>](upread.md)

