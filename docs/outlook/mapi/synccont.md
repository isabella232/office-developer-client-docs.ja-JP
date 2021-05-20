---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430407"
---
# <a name="synccont"></a><span data-ttu-id="30f29-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="30f29-103">SYNCCONT</span></span>

<span data-ttu-id="30f29-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30f29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30f29-105">ローカル ストア内の指定されたフォルダーの内容を、コンテンツの同期状態中にサーバーと同期する [情報](synchronize-contents-state.md)です。</span><span class="sxs-lookup"><span data-stu-id="30f29-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="30f29-106">これには、アップロードだけ、またはアップロードとダウンロードを含む完全な同期が含まれる。</span><span class="sxs-lookup"><span data-stu-id="30f29-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30f29-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="30f29-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="30f29-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="30f29-108">Members</span></span>

<span data-ttu-id="30f29-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30f29-109">_ulFlags_</span></span>
  
> <span data-ttu-id="30f29-110">[in]同期中に適切な動作を判断するフラグ。</span><span class="sxs-lookup"><span data-stu-id="30f29-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="30f29-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="30f29-111">UPC_OK</span></span>
    
  - <span data-ttu-id="30f29-112">[in]アップロードまたは完全同期が成功しました。</span><span class="sxs-lookup"><span data-stu-id="30f29-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="30f29-113">クライアントは、情報をサーバーと同期した後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="30f29-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="30f29-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="30f29-114">_iEnt_</span></span>
  
> <span data-ttu-id="30f29-115">[out]インデックスを使用して、cEnt で指定されたフォルダー数のコンテンツの同期  _を追跡します_。</span><span class="sxs-lookup"><span data-stu-id="30f29-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="30f29-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="30f29-116">_cEnt_</span></span>
  
> <span data-ttu-id="30f29-117">[out]レプリケートするフォルダーの数。</span><span class="sxs-lookup"><span data-stu-id="30f29-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="30f29-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="30f29-118">_pvReserved_</span></span>
  
> <span data-ttu-id="30f29-119">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="30f29-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="30f29-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="30f29-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="30f29-121">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="30f29-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="30f29-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="30f29-122">_psosReserved_</span></span>
  
> <span data-ttu-id="30f29-123">このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="30f29-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="30f29-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="30f29-124">See also</span></span>

- [<span data-ttu-id="30f29-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="30f29-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="30f29-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="30f29-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="30f29-127">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="30f29-127">MAPI Constants</span></span>](mapi-constants.md)

