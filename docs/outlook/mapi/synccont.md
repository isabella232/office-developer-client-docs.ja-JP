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
# <a name="synccont"></a><span data-ttu-id="19235-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="19235-103">SYNCCONT</span></span>

<span data-ttu-id="19235-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19235-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19235-105">[コンテンツ同期状態](synchronize-contents-state.md)の間に、ローカルストア内の指定したフォルダーの内容をサーバーと同期するための情報。</span><span class="sxs-lookup"><span data-stu-id="19235-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="19235-106">これにはアップロードのみが含まれます。または、アップロードとダウンロードを含む完全同期を行います。</span><span class="sxs-lookup"><span data-stu-id="19235-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="19235-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="19235-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="19235-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="19235-108">Members</span></span>

<span data-ttu-id="19235-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="19235-109">_ulFlags_</span></span>
  
> <span data-ttu-id="19235-110">順番同期時に適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="19235-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="19235-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="19235-111">UPC_OK</span></span>
    
  - <span data-ttu-id="19235-112">順番アップロードまたは完全同期が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="19235-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="19235-113">クライアントは、情報をサーバーと同期した後にこれを設定します。</span><span class="sxs-lookup"><span data-stu-id="19235-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="19235-114">_ient_</span><span class="sxs-lookup"><span data-stu-id="19235-114">_iEnt_</span></span>
  
> <span data-ttu-id="19235-115">読み上げによって指定されたフォルダーの数について__ のコンテンツの同期を追跡するインデックス。</span><span class="sxs-lookup"><span data-stu-id="19235-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="19235-116">_fea-cent-logging-service_</span><span class="sxs-lookup"><span data-stu-id="19235-116">_cEnt_</span></span>
  
> <span data-ttu-id="19235-117">読み上げレプリケートするフォルダーの数。</span><span class="sxs-lookup"><span data-stu-id="19235-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="19235-118">_pvreserved_</span><span class="sxs-lookup"><span data-stu-id="19235-118">_pvReserved_</span></span>
  
> <span data-ttu-id="19235-119">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="19235-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="19235-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="19235-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="19235-121">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="19235-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="19235-122">_psosreserved_</span><span class="sxs-lookup"><span data-stu-id="19235-122">_psosReserved_</span></span>
  
> <span data-ttu-id="19235-123">このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="19235-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="19235-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="19235-124">See also</span></span>

- [<span data-ttu-id="19235-125">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="19235-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="19235-126">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="19235-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="19235-127">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="19235-127">MAPI Constants</span></span>](mapi-constants.md)

