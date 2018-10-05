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
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398123"
---
# <a name="dntbl"></a><span data-ttu-id="132fd-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="132fd-103">DNTBL</span></span>
 
<span data-ttu-id="132fd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="132fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="132fd-105">ストアの内容の完全な同期の一部として、[テーブルの状態をダウンロード](download-table-state.md)、実行中にサーバーからフォルダーの内容をダウンロードするための情報です。</span><span class="sxs-lookup"><span data-stu-id="132fd-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="132fd-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="132fd-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="132fd-107">Members</span><span class="sxs-lookup"><span data-stu-id="132fd-107">Members</span></span>

<span data-ttu-id="132fd-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="132fd-108">_ulFlags_</span></span>
  
> <span data-ttu-id="132fd-109">[in]フラグの動作を変更するのには</span><span class="sxs-lookup"><span data-stu-id="132fd-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="132fd-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="132fd-110">DNT_OK</span></span>
    
    - <span data-ttu-id="132fd-111">[in]ダウンロードが正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="132fd-111">[in] Download was successful.</span></span> <span data-ttu-id="132fd-112">クライアントは、サーバーから情報をダウンロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="132fd-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="132fd-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="132fd-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="132fd-114">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="132fd-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="132fd-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="132fd-116">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="132fd-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="132fd-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="132fd-118">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="132fd-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="132fd-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="132fd-120">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="132fd-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="132fd-121">_pxicc_</span></span>
  
>  <span data-ttu-id="132fd-122">[out]コンテンツの変更のダウンロードをサポートする**IExchangeImportContentsChanges**の内容のインターフェイスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="132fd-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="132fd-123">**IExchangeImportContentsChanges**の詳細については、 [ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="132fd-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="132fd-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="132fd-124">_pxihc_</span></span>
  
>  <span data-ttu-id="132fd-125">[out]**IExchangeImportHierarchyChanges**階層のインターフェイスへのポインターをサポートする階層の増分変更をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="132fd-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="132fd-126">**IExchangeImportHierarchyChanges**の詳細については、 [ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="132fd-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="132fd-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="132fd-127">_pszName_</span></span>
  
>  <span data-ttu-id="132fd-128">[out]フォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="132fd-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="132fd-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="132fd-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="132fd-130">[out]フォルダーの最終更新時刻。</span><span class="sxs-lookup"><span data-stu-id="132fd-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="132fd-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="132fd-131">_ulRights_</span></span>
  
>  <span data-ttu-id="132fd-132">[out]フォルダーの**[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** プロパティの値です。</span><span class="sxs-lookup"><span data-stu-id="132fd-132">[out] Value of the **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="132fd-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="132fd-133">_feid_</span></span>
  
>  <span data-ttu-id="132fd-134">[out]フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="132fd-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="132fd-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="132fd-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="132fd-136">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="132fd-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="132fd-137">_rgte_</span></span>
  
> <span data-ttu-id="132fd-138">[out]通常 (または非表示) の変更と関連付けられている (非表示) の項目です。</span><span class="sxs-lookup"><span data-stu-id="132fd-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="132fd-139">*rgte [0]* は、通常の項目については、 *rgte [1]* 関連付けられているアイテムです。</span><span class="sxs-lookup"><span data-stu-id="132fd-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="132fd-140">Outlook では、増分変更の同期 (ICS) を使用する場合は、ダウンロード中にこのメンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="132fd-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="132fd-141">ICS の詳細については、 [ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="132fd-141">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="132fd-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="132fd-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="132fd-143">[の] [out] このメンバーは、Outlook の内部使用に予約して、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="132fd-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="132fd-144">_boReserved_</span></span>
  
>  <span data-ttu-id="132fd-145">[in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="132fd-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="132fd-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="132fd-147">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="132fd-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="132fd-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="132fd-149">[in]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="132fd-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="132fd-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="132fd-150">See also</span></span>

- [<span data-ttu-id="132fd-151">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="132fd-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="132fd-152">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="132fd-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="132fd-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="132fd-153">DNTBLE</span></span>](dntble.md)

