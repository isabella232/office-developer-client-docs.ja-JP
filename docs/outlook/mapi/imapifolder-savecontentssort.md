---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411618"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="36956-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="36956-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="36956-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36956-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36956-105">フォルダーのコンテンツ テーブルの既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="36956-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="36956-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="36956-106">Parameters</span></span>

 <span data-ttu-id="36956-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="36956-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="36956-108">[in]既定の並べ替え順序を含む [SSortOrderSet](ssortorderset.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="36956-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="36956-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36956-109">_ulFlags_</span></span>
  
> <span data-ttu-id="36956-110">[in]既定の並べ替え順序の設定方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="36956-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="36956-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="36956-111">The following flag can be set:</span></span>
    
<span data-ttu-id="36956-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="36956-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="36956-113">既定の並べ替え順序セットは、指定されたフォルダーとそのすべてのサブフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="36956-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36956-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="36956-114">Return value</span></span>

<span data-ttu-id="36956-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="36956-115">S_OK</span></span> 
  
> <span data-ttu-id="36956-116">並べ替え順序が正常に保存されました。</span><span class="sxs-lookup"><span data-stu-id="36956-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="36956-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="36956-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="36956-118">メッセージ ストア プロバイダーは、フォルダーコンテンツ テーブルの並べ替え順序の保存をサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="36956-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36956-119">注釈</span><span class="sxs-lookup"><span data-stu-id="36956-119">Remarks</span></span>

<span data-ttu-id="36956-120">**IMAPIFolder::SaveContentsSort** メソッドは、フォルダーのコンテンツ テーブルの既定の並べ替え順序を確立します。</span><span class="sxs-lookup"><span data-stu-id="36956-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="36956-121">つまり、コードが **SaveContentsSort** を呼び出した後にクライアントがフォルダーの [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出す場合、返されるコンテンツ テーブルの行は **SaveContentsSort** によって確立された順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="36956-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="36956-122">すべてのメッセージ ストア プロバイダーが **SaveContentsSort をサポートしているのではありません**。メッセージ ストア プロバイダーが **SaveContentsSort** メソッドからMAPI_E_NO_SUPPORTを返すのは許容されます。</span><span class="sxs-lookup"><span data-stu-id="36956-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36956-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="36956-123">See also</span></span>



[<span data-ttu-id="36956-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="36956-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="36956-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="36956-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="36956-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="36956-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

