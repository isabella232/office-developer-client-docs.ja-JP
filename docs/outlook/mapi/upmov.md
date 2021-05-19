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
# <a name="upmov"></a><span data-ttu-id="0cd24-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="0cd24-103">UPMOV</span></span>
 
<span data-ttu-id="0cd24-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cd24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cd24-105">移動されたアイテムをアップロードする情報。</span><span class="sxs-lookup"><span data-stu-id="0cd24-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="0cd24-106">この情報は、アップロードの削除状態とアップロード[テーブルの状態](upload-delete-status-state.md)[の間に使用されます](upload-table-state.md)。</span><span class="sxs-lookup"><span data-stu-id="0cd24-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0cd24-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0cd24-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="0cd24-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="0cd24-108">Members</span></span>

<span data-ttu-id="0cd24-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0cd24-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0cd24-110">[in]アップロード中の適切な動作を決定するフラグ。</span><span class="sxs-lookup"><span data-stu-id="0cd24-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="0cd24-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="0cd24-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="0cd24-112">[in]サーバー フォルダーを開く際に問題が発生しました。</span><span class="sxs-lookup"><span data-stu-id="0cd24-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="0cd24-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="0cd24-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="0cd24-114">[in]アップロードの状態が変更されました。</span><span class="sxs-lookup"><span data-stu-id="0cd24-114">[in] The upload state has changed.</span></span> <span data-ttu-id="0cd24-115">これは、クライアントがローカル ストアの状態の変更を追跡するために使用します。</span><span class="sxs-lookup"><span data-stu-id="0cd24-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="0cd24-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="0cd24-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="0cd24-117">[in]アップロード状態のコミット。</span><span class="sxs-lookup"><span data-stu-id="0cd24-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="0cd24-118">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="0cd24-118">_pReserved_</span></span>
  
>  <span data-ttu-id="0cd24-119">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0cd24-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="0cd24-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="0cd24-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="0cd24-121">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0cd24-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="0cd24-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="0cd24-122">_pszName_</span></span>
  
>  <span data-ttu-id="0cd24-123">[out]移動先フォルダーの名前。</span><span class="sxs-lookup"><span data-stu-id="0cd24-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="0cd24-124">このメンバーは UNICODE をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="0cd24-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="0cd24-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="0cd24-125">_feid_</span></span>
  
>  <span data-ttu-id="0cd24-126">[out]移動先フォルダーのエントリ ID。</span><span class="sxs-lookup"><span data-stu-id="0cd24-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="0cd24-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="0cd24-127">_pfld_</span></span>
  
>  <span data-ttu-id="0cd24-128">[in]サーバー フォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0cd24-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="0cd24-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="0cd24-129">_pxicc_</span></span>
  
>  <span data-ttu-id="0cd24-130">[in]増分変更同期 (ICS) を使用する場合のコンテンツ変更のアップロードをサポートする **IExchangeImportContentsChanges** コンテンツ インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0cd24-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="0cd24-131">**IExchangeImportContentsChanges** および ICS の詳細については [、「ICS 評価基準」を参照してください](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0cd24-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="0cd24-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="0cd24-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="0cd24-133">[out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0cd24-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="0cd24-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="0cd24-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="0cd24-135">[out]次の移動コンテキスト。</span><span class="sxs-lookup"><span data-stu-id="0cd24-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="0cd24-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="0cd24-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="0cd24-137">[in]ここに移動したアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="0cd24-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0cd24-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="0cd24-138">See also</span></span>

- [<span data-ttu-id="0cd24-139">レプリケーション API について</span><span class="sxs-lookup"><span data-stu-id="0cd24-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="0cd24-140">レプリケーション状態のマシンについて</span><span class="sxs-lookup"><span data-stu-id="0cd24-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="0cd24-141">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="0cd24-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="0cd24-142">FEID</span><span class="sxs-lookup"><span data-stu-id="0cd24-142">FEID</span></span>](feid.md)

