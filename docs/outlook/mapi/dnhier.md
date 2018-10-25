---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389086"
---
# <a name="dnhier"></a><span data-ttu-id="e3085-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="e3085-103">DNHIER</span></span>

<span data-ttu-id="e3085-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3085-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3085-105">階層の完全同期の一部である[階層状態のダウンロード](download-hierarchy-state.md)中に、サーバーから階層をダウンロードするための情報です。</span><span class="sxs-lookup"><span data-stu-id="e3085-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="e3085-106">このダウンロード手順では、Microsoft Exchange の増分変更の同期 (ICS) を使用します。</span><span class="sxs-lookup"><span data-stu-id="e3085-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="e3085-107">ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3085-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e3085-108">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e3085-108">Quick Info</span></span>

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

## <a name="members"></a><span data-ttu-id="e3085-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="e3085-109">Members</span></span>

<span data-ttu-id="e3085-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3085-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="e3085-111">[in] ダウンロード中の適切な動作を決定するフラグです。</span><span class="sxs-lookup"><span data-stu-id="e3085-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="e3085-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="e3085-112">DNH_OK</span></span>
    
   - <span data-ttu-id="e3085-113">[in] ダウンロードに成功しました。</span><span class="sxs-lookup"><span data-stu-id="e3085-113">[in] Download was successful.</span></span> <span data-ttu-id="e3085-114">クライアントは、サーバーから情報をダウンロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="e3085-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="e3085-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="e3085-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="e3085-116">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e3085-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e3085-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="e3085-117">_pxihc_</span></span>
  
>  <span data-ttu-id="e3085-118">[out] 階層の増分変更のダウンロードをサポートする、**IExchangeImportHierarchyChanges** の階層インターフェイスのポインターです。</span><span class="sxs-lookup"><span data-stu-id="e3085-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="e3085-119">**IExchangeImportHierarchyChanges** の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3085-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="e3085-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="e3085-120">_cEntNew_</span></span>
  
> <span data-ttu-id="e3085-121">[out] ローカル ストアに追加されたフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="e3085-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="e3085-122">ICS を使用してダウンロードしている間に Outlook がこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="e3085-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="e3085-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="e3085-123">_cEntMod_</span></span>
  
> <span data-ttu-id="e3085-124">[out] ローカル ストアで変更されるフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="e3085-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="e3085-125">ICS を使用してダウンロードしている間に Outlook がこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="e3085-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="e3085-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="e3085-126">_cEntDel_</span></span>
  
> <span data-ttu-id="e3085-127">[out] ローカル ストアで削除されるフォルダーの数です。</span><span class="sxs-lookup"><span data-stu-id="e3085-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="e3085-128">ICS を使用してダウンロードしている間に Outlook がこの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="e3085-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3085-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e3085-129">See also</span></span>

- [<span data-ttu-id="e3085-130">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="e3085-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="e3085-131">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="e3085-131">MAPI Constants</span></span>](mapi-constants.md)

