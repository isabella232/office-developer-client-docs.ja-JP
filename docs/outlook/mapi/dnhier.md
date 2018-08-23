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
ms.openlocfilehash: 3c7d59849fcd66a5fe90623b7bb8516d13b4a2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799968"
---
# <a name="dnhier"></a><span data-ttu-id="81a63-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="81a63-103">DNHIER</span></span>

<span data-ttu-id="81a63-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81a63-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81a63-105">階層サーバーからのダウンロード、[階層の状態をダウンロード](download-hierarchy-state.md)する時に完全な階層の同期の一部の情報です。</span><span class="sxs-lookup"><span data-stu-id="81a63-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="81a63-106">このダウンロードのプロセスでは、Microsoft Exchange 増分変更の同期 (ICS) を使用します。</span><span class="sxs-lookup"><span data-stu-id="81a63-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="81a63-107">ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81a63-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="81a63-108">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="81a63-108">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="81a63-109">Members</span><span class="sxs-lookup"><span data-stu-id="81a63-109">Members</span></span>

<span data-ttu-id="81a63-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81a63-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="81a63-111">[in]ダウンロード中に適切な動作を決定するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="81a63-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="81a63-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="81a63-112">DNH_OK</span></span>
    
   - <span data-ttu-id="81a63-113">[in]ダウンロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="81a63-113">[in] Download was successful.</span></span> <span data-ttu-id="81a63-114">クライアントは、サーバーから情報をダウンロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="81a63-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="81a63-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="81a63-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="81a63-116">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="81a63-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="81a63-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="81a63-117">_pxihc_</span></span>
  
>  <span data-ttu-id="81a63-118">[out]**IExchangeImportHierarchyChanges**階層のインターフェイスへのポインターをサポートする階層の増分変更をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="81a63-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="81a63-119">**IExchangeImportHierarchyChanges**の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81a63-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="81a63-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="81a63-120">_cEntNew_</span></span>
  
> <span data-ttu-id="81a63-121">[out]ローカル ストアに追加するフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="81a63-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="81a63-122">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="81a63-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="81a63-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="81a63-123">_cEntMod_</span></span>
  
> <span data-ttu-id="81a63-124">[out]ローカル ストアを変更するフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="81a63-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="81a63-125">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="81a63-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="81a63-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="81a63-126">_cEntDel_</span></span>
  
> <span data-ttu-id="81a63-127">[out]ローカル ストアから削除するフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="81a63-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="81a63-128">Outlook では、ICS を使用する場合は、ダウンロード中にこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="81a63-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81a63-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="81a63-129">See also</span></span>

- [<span data-ttu-id="81a63-130">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="81a63-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="81a63-131">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="81a63-131">MAPI Constants</span></span>](mapi-constants.md)

