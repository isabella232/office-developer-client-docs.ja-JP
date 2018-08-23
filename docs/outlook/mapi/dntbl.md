---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: 72dd2a27e89f00885710125f4ecb68be65f2185e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567700"
---
# <a name="dntbl"></a><span data-ttu-id="6a700-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="6a700-103">DNTBL</span></span>
 
<span data-ttu-id="6a700-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a700-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a700-105">ストアの内容の完全な同期の一部として、[テーブルの状態をダウンロード](download-table-state.md)、実行中にサーバーからフォルダーの内容をダウンロードするための情報です。</span><span class="sxs-lookup"><span data-stu-id="6a700-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6a700-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="6a700-106">Quick info</span></span>

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a><span data-ttu-id="6a700-107">Members</span><span class="sxs-lookup"><span data-stu-id="6a700-107">Members</span></span>

<span data-ttu-id="6a700-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6a700-108">_ulFlags_</span></span>
  
> <span data-ttu-id="6a700-109">[in]フラグの動作を変更するのには</span><span class="sxs-lookup"><span data-stu-id="6a700-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="6a700-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="6a700-110">DNT_OK</span></span>
    
    - <span data-ttu-id="6a700-111">[in]ダウンロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="6a700-111">[in] Download was successful.</span></span> <span data-ttu-id="6a700-112">クライアントは、サーバーから情報をダウンロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="6a700-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="6a700-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="6a700-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="6a700-114">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6a700-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="6a700-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="6a700-116">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6a700-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="6a700-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="6a700-118">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6a700-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="6a700-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="6a700-120">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6a700-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="6a700-121">_pxicc_</span></span>
  
>  <span data-ttu-id="6a700-122">[out]コンテンツの変更のダウンロードをサポートする**IExchangeImportContentsChanges**の内容のインターフェイスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="6a700-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="6a700-123">**IExchangeImportContentsChanges**の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a700-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="6a700-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="6a700-124">_pxihc_</span></span>
  
>  <span data-ttu-id="6a700-125">[out]**IExchangeImportHierarchyChanges**階層のインターフェイスへのポインターをサポートする階層の増分変更をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6a700-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="6a700-126">**IExchangeImportHierarchyChanges**の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a700-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="6a700-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="6a700-127">_pszName_</span></span>
  
>  <span data-ttu-id="6a700-128">[out]フォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="6a700-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="6a700-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="6a700-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="6a700-130">[out]フォルダーの最終更新時刻。</span><span class="sxs-lookup"><span data-stu-id="6a700-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="6a700-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="6a700-131">_ulRights_</span></span>
  
>  <span data-ttu-id="6a700-132">[out]フォルダーの**[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** プロパティの値です。</span><span class="sxs-lookup"><span data-stu-id="6a700-132">[out] Value of the **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="6a700-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="6a700-133">_feid_</span></span>
  
>  <span data-ttu-id="6a700-134">[out]フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="6a700-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="6a700-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="6a700-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="6a700-136">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6a700-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="6a700-137">_rgte_</span></span>
  
> <span data-ttu-id="6a700-138">[out]通常 (または非表示) の変更と関連付けられている (非表示) の項目です。</span><span class="sxs-lookup"><span data-stu-id="6a700-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="6a700-139">*rgte [0]* は、通常の項目については、 *rgte [1]* 関連付けられているアイテムです。</span><span class="sxs-lookup"><span data-stu-id="6a700-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="6a700-140">Outlook では、増分変更の同期 (ICS) を使用する場合は、ダウンロード中にこのメンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="6a700-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="6a700-141">ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a700-141">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="6a700-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="6a700-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="6a700-143">[の] [out] このメンバーは、Outlook の内部使用に予約して、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6a700-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="6a700-144">_boReserved_</span></span>
  
>  <span data-ttu-id="6a700-145">[in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6a700-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="6a700-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="6a700-147">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="6a700-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="6a700-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="6a700-149">[in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6a700-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6a700-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a700-150">See also</span></span>

- [<span data-ttu-id="6a700-151">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="6a700-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="6a700-152">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="6a700-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="6a700-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="6a700-153">DNTBLE</span></span>](dntble.md)

