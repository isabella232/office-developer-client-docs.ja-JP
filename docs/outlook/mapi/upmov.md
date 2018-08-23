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
ms.openlocfilehash: 0a8e318f9bb5e538473e1b60c650e8730f692e50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577990"
---
# <a name="upmov"></a><span data-ttu-id="2c4ae-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="2c4ae-103">UPMOV</span></span>
 
<span data-ttu-id="2c4ae-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c4ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c4ae-105">移動されたアイテムをアップロードする方法の詳細については。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="2c4ae-106">[アップロード ステータスの状態を削除](upload-delete-status-state.md)し、[テーブルの状態をアップロード](upload-table-state.md)中には、この情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2c4ae-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="2c4ae-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="2c4ae-108">Members</span><span class="sxs-lookup"><span data-stu-id="2c4ae-108">Members</span></span>

<span data-ttu-id="2c4ae-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2c4ae-110">[in]アップロード中に適切な動作を決定するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="2c4ae-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="2c4ae-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="2c4ae-112">[in]サーバーのフォルダーを開くときに問題です。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="2c4ae-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="2c4ae-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="2c4ae-114">[in]アップロードの状態が変更されました。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-114">[in] The upload state has changed.</span></span> <span data-ttu-id="2c4ae-115">ローカル ストアの状態の変更を追跡するためにクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="2c4ae-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="2c4ae-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="2c4ae-117">[in]アップロード状態をコミットします。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="2c4ae-118">_保持_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-118">_pReserved_</span></span>
  
>  <span data-ttu-id="2c4ae-119">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="2c4ae-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="2c4ae-121">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="2c4ae-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-122">_pszName_</span></span>
  
>  <span data-ttu-id="2c4ae-123">[out]コピー先のフォルダーの名前です。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="2c4ae-124">このメンバーは、UNICODE をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="2c4ae-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-125">_feid_</span></span>
  
>  <span data-ttu-id="2c4ae-126">[out]コピー先のフォルダーのエントリ ID です。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="2c4ae-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-127">_pfld_</span></span>
  
>  <span data-ttu-id="2c4ae-128">[in]サーバー フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="2c4ae-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-129">_pxicc_</span></span>
  
>  <span data-ttu-id="2c4ae-130">[in]増分変更の同期 (ICS) を使用する場合、コンテンツの変更のアップロードをサポートする**IExchangeImportContentsChanges**の内容のインターフェイスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="2c4ae-131">**IExchangeImportContentsChanges**と ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="2c4ae-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="2c4ae-133">[out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="2c4ae-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="2c4ae-135">[out]次にコンテキストを移動します。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="2c4ae-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="2c4ae-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="2c4ae-137">[in]項目の番号をここに移動します。</span><span class="sxs-lookup"><span data-stu-id="2c4ae-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2c4ae-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c4ae-138">See also</span></span>

- [<span data-ttu-id="2c4ae-139">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="2c4ae-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="2c4ae-140">レプリケーション ステート マシンについて</span><span class="sxs-lookup"><span data-stu-id="2c4ae-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="2c4ae-141">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="2c4ae-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="2c4ae-142">FEID</span><span class="sxs-lookup"><span data-stu-id="2c4ae-142">FEID</span></span>](feid.md)

