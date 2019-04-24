---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339187"
---
# <a name="upmov"></a><span data-ttu-id="e32a6-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="e32a6-103">UPMOV</span></span>
 
<span data-ttu-id="e32a6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e32a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e32a6-105">移動されたアイテムをアップロードするための情報。</span><span class="sxs-lookup"><span data-stu-id="e32a6-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="e32a6-106">この情報は、削除の状態を[アップロード](upload-delete-status-state.md)し、[テーブルの状態](upload-table-state.md)をアップロードするときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="e32a6-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e32a6-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e32a6-107">Quick info</span></span>

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a><span data-ttu-id="e32a6-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="e32a6-108">Members</span></span>

<span data-ttu-id="e32a6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e32a6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e32a6-110">順番アップロード中の適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="e32a6-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="e32a6-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="e32a6-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="e32a6-112">順番サーバーフォルダーを開くときに問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="e32a6-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="e32a6-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="e32a6-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="e32a6-114">順番アップロード状態が変更されました。</span><span class="sxs-lookup"><span data-stu-id="e32a6-114">[in] The upload state has changed.</span></span> <span data-ttu-id="e32a6-115">これは、クライアントがローカルストアの状態の変更を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e32a6-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="e32a6-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="e32a6-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="e32a6-117">順番アップロード状態をコミットします。</span><span class="sxs-lookup"><span data-stu-id="e32a6-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="e32a6-118">_保持され_</span><span class="sxs-lookup"><span data-stu-id="e32a6-118">_pReserved_</span></span>
  
>  <span data-ttu-id="e32a6-119">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e32a6-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e32a6-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="e32a6-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="e32a6-121">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e32a6-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e32a6-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="e32a6-122">_pszName_</span></span>
  
>  <span data-ttu-id="e32a6-123">読み上げ宛先フォルダーの名前。</span><span class="sxs-lookup"><span data-stu-id="e32a6-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="e32a6-124">このメンバーは UNICODE をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="e32a6-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="e32a6-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="e32a6-125">_feid_</span></span>
  
>  <span data-ttu-id="e32a6-126">読み上げ宛先フォルダーのエントリ ID。</span><span class="sxs-lookup"><span data-stu-id="e32a6-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="e32a6-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="e32a6-127">_pfld_</span></span>
  
>  <span data-ttu-id="e32a6-128">順番サーバーフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e32a6-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="e32a6-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="e32a6-129">_pxicc_</span></span>
  
>  <span data-ttu-id="e32a6-130">順番増分変更の同期 (ICS) を使用した場合のコンテンツの変更のアップロードをサポートする、 **iexchangeimportcontents changes**コンテンツインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e32a6-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="e32a6-131">**iexchangeimportの内容の変更**および ics の詳細については、「 [ics の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e32a6-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="e32a6-132">_dwreserved_</span><span class="sxs-lookup"><span data-stu-id="e32a6-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="e32a6-133">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e32a6-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e32a6-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="e32a6-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="e32a6-135">読み上げ次の移動コンテキスト。</span><span class="sxs-lookup"><span data-stu-id="e32a6-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="e32a6-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="e32a6-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="e32a6-137">順番ここで移動したアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="e32a6-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e32a6-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="e32a6-138">See also</span></span>

- [<span data-ttu-id="e32a6-139">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="e32a6-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="e32a6-140">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="e32a6-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e32a6-141">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="e32a6-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="e32a6-142">FEID</span><span class="sxs-lookup"><span data-stu-id="e32a6-142">FEID</span></span>](feid.md)

