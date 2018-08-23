---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: fbf064201bf8d2733c3eea1e1a24f77b146a23c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564571"
---
# <a name="dnhier"></a><span data-ttu-id="dfd6e-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="dfd6e-103">DNHIER</span></span>

<span data-ttu-id="dfd6e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfd6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfd6e-105">階層サーバーからのダウンロード、[階層の状態をダウンロード](download-hierarchy-state.md)する時に完全な階層の同期の一部の情報です。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="dfd6e-106">このダウンロードのプロセスでは、Microsoft Exchange 増分変更の同期 (ICS) を使用します。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="dfd6e-107">ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dfd6e-108">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="dfd6e-108">Quick info</span></span>

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="dfd6e-109">Members</span><span class="sxs-lookup"><span data-stu-id="dfd6e-109">Members</span></span>

<span data-ttu-id="dfd6e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dfd6e-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="dfd6e-111">[in]ダウンロード中に適切な動作を決定するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="dfd6e-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="dfd6e-112">DNH_OK</span></span>
    
   - <span data-ttu-id="dfd6e-113">[in]ダウンロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-113">[in] Download was successful.</span></span> <span data-ttu-id="dfd6e-114">クライアントは、サーバーから情報をダウンロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="dfd6e-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="dfd6e-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="dfd6e-116">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="dfd6e-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="dfd6e-117">_pxihc_</span></span>
  
>  <span data-ttu-id="dfd6e-118">[out]**IExchangeImportHierarchyChanges**階層のインターフェイスへのポインターをサポートする階層の増分変更をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="dfd6e-119">**IExchangeImportHierarchyChanges**の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="dfd6e-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="dfd6e-120">_cEntNew_</span></span>
  
> <span data-ttu-id="dfd6e-121">[out]ローカル ストアに追加するフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="dfd6e-122">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="dfd6e-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="dfd6e-123">_cEntMod_</span></span>
  
> <span data-ttu-id="dfd6e-124">[out]ローカル ストアを変更するフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="dfd6e-125">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="dfd6e-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="dfd6e-126">_cEntDel_</span></span>
  
> <span data-ttu-id="dfd6e-127">[out]ローカル ストアから削除するフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="dfd6e-128">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="dfd6e-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfd6e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfd6e-129">See also</span></span>

- [<span data-ttu-id="dfd6e-130">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="dfd6e-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="dfd6e-131">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="dfd6e-131">MAPI Constants</span></span>](mapi-constants.md)

