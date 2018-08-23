---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b1ab1bd4eb6badc75065ce54d009e034f0fc2b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584675"
---
# <a name="synccont"></a><span data-ttu-id="a8bf8-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="a8bf8-103">SYNCCONT</span></span>

<span data-ttu-id="a8bf8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8bf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8bf8-105">[内容の状態を同期](synchronize-contents-state.md)する際にサーバーとローカル ストア内の指定したフォルダーの内容を同期するための情報です。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="a8bf8-106">これだけのアップロード、またはアップロードし、ダウンロードを含む完全な同期が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8bf8-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a8bf8-107">Quick info</span></span>

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a><span data-ttu-id="a8bf8-108">Members</span><span class="sxs-lookup"><span data-stu-id="a8bf8-108">Members</span></span>

<span data-ttu-id="a8bf8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8bf8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a8bf8-110">[in]同期中に適切な動作を決定するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="a8bf8-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="a8bf8-111">UPC_OK</span></span>
    
  - <span data-ttu-id="a8bf8-112">[in]アップロードまたは完全な同期が成功しました。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="a8bf8-113">クライアントでは、情報をサーバーと同期した後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="a8bf8-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="a8bf8-114">_iEnt_</span></span>
  
> <span data-ttu-id="a8bf8-115">[out]_セント_で指定されたフォルダーの内容の同期を追跡するためにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="a8bf8-116">_セント_</span><span class="sxs-lookup"><span data-stu-id="a8bf8-116">_cEnt_</span></span>
  
> <span data-ttu-id="a8bf8-117">[out]レプリケートするフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="a8bf8-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="a8bf8-118">_pvReserved_</span></span>
  
> <span data-ttu-id="a8bf8-119">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="a8bf8-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="a8bf8-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="a8bf8-121">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="a8bf8-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="a8bf8-122">_psosReserved_</span></span>
  
> <span data-ttu-id="a8bf8-123">このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a8bf8-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a8bf8-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8bf8-124">See also</span></span>

- [<span data-ttu-id="a8bf8-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="a8bf8-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="a8bf8-126">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="a8bf8-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="a8bf8-127">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="a8bf8-127">MAPI Constants</span></span>](mapi-constants.md)

