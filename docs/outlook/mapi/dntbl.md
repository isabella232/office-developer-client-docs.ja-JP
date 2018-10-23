---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '最終更新日: 2012 年 7 月 5 日'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398123"
---
# <a name="dntbl"></a><span data-ttu-id="093e1-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="093e1-103">DNTBL</span></span>
 
<span data-ttu-id="093e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="093e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="093e1-105">ストアの内容の完全同期の一部として、[テーブルの状態をダウンロード](download-table-state.md)中に、サーバーからフォルダーの内容をダウンロードするための情報です。</span><span class="sxs-lookup"><span data-stu-id="093e1-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="093e1-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="093e1-106">Quick Info</span></span>

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

## <a name="members"></a><span data-ttu-id="093e1-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="093e1-107">Members</span></span>

<span data-ttu-id="093e1-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="093e1-108">_ulFlags_</span></span>
  
> <span data-ttu-id="093e1-109">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="093e1-109">[in] Flags to modify behavior.</span></span> 
    
  - <span data-ttu-id="093e1-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="093e1-110">DNT_OK</span></span>
    
    - <span data-ttu-id="093e1-111">[in]ダウンロードに成功しました。</span><span class="sxs-lookup"><span data-stu-id="093e1-111">[in] Download was successful.</span></span> <span data-ttu-id="093e1-112">クライアントは、サーバーから情報をダウンロードした後、これを設定します。</span><span class="sxs-lookup"><span data-stu-id="093e1-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="093e1-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="093e1-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="093e1-114">[out]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="093e1-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="093e1-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="093e1-116">[out]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="093e1-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="093e1-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="093e1-118">[out]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="093e1-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="093e1-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="093e1-120">[out]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="093e1-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="093e1-121">_pxicc_</span></span>
  
>  <span data-ttu-id="093e1-122">[out] 内容変更のダウンロードをサポートする、**IExchangeImportContentsChanges**の内容インターフェイスのポインターです。</span><span class="sxs-lookup"><span data-stu-id="093e1-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="093e1-123">**IExchangeImportContentsChanges**の詳細については、[ICSの評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="093e1-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="093e1-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="093e1-124">_pxihc_</span></span>
  
>  <span data-ttu-id="093e1-125">[out]階層の増分変更のダウンロードをサポートする、**IExchangeImportHierarchyChanges**の階層インターフェイスのポインターです。</span><span class="sxs-lookup"><span data-stu-id="093e1-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="093e1-126">**IExchangeImportHierarchyChanges**の詳細については、[ICSの評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="093e1-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="093e1-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="093e1-127">_pszName_</span></span>
  
>  <span data-ttu-id="093e1-128">[out]フォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="093e1-128">Name of the folder.</span></span> 
    
<span data-ttu-id="093e1-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="093e1-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="093e1-130">[out]フォルダーの最終変更時刻。</span><span class="sxs-lookup"><span data-stu-id="093e1-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="093e1-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="093e1-131">_ulRights_</span></span>
  
>  <span data-ttu-id="093e1-132">[out]フォルダーの**[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** プロパティの値です。</span><span class="sxs-lookup"><span data-stu-id="093e1-132">[out] Value of the **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="093e1-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="093e1-133">_FEID_</span></span>
  
>  <span data-ttu-id="093e1-134">[out]フォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="093e1-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="093e1-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="093e1-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="093e1-136">[out]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="093e1-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="093e1-137">_rgte_</span></span>
  
> <span data-ttu-id="093e1-138">[out]通常 (または表示) アイテムと関連する (または非表示) アイテムの変更。</span><span class="sxs-lookup"><span data-stu-id="093e1-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="093e1-139">*rgte [0]* は通常アイテム、*rgte [1]* は関連するアイテムに使います。</span><span class="sxs-lookup"><span data-stu-id="093e1-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="093e1-140">増分変更の同期 (ICS) を使用してダウンロードしている間に Outlook がこのメンバーを設定します。</span><span class="sxs-lookup"><span data-stu-id="093e1-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="093e1-141">ICSの詳細については、[ICSの評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="093e1-141">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="093e1-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="093e1-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="093e1-143">[in]/[out]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="093e1-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="093e1-144">_boReserved_</span></span>
  
>  <span data-ttu-id="093e1-145">[in]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="093e1-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="093e1-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="093e1-147">[out]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="093e1-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="093e1-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="093e1-149">[in]このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="093e1-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="093e1-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="093e1-150">See also</span></span>

- [<span data-ttu-id="093e1-151">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="093e1-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="093e1-152">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="093e1-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="093e1-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="093e1-153">DNTBLE</span></span>](dntble.md)

