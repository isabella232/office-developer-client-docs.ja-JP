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
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="5a7b1-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="5a7b1-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="5a7b1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a7b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a7b1-105">フォルダーの contents テーブルの既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5a7b1-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5a7b1-106">Parameters</span></span>

 <span data-ttu-id="5a7b1-107">_lpsortcriteria_</span><span class="sxs-lookup"><span data-stu-id="5a7b1-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="5a7b1-108">順番既定の並べ替え順序を含む[ssortorderset](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="5a7b1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a7b1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5a7b1-110">順番既定の並べ替え順序を設定する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="5a7b1-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="5a7b1-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="5a7b1-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="5a7b1-113">既定の並べ替え順序セットは、指定したフォルダーとそのすべてのサブフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a7b1-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="5a7b1-114">Return value</span></span>

<span data-ttu-id="5a7b1-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a7b1-115">S_OK</span></span> 
  
> <span data-ttu-id="5a7b1-116">並べ替え順序が正常に保存されました。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="5a7b1-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5a7b1-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5a7b1-118">メッセージストアプロバイダーは、フォルダーコンテンツテーブルの並べ替え順序の保存をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5a7b1-119">注釈</span><span class="sxs-lookup"><span data-stu-id="5a7b1-119">Remarks</span></span>

<span data-ttu-id="5a7b1-120">**imapifolder:: SaveContentsSort**メソッドは、フォルダーの contents テーブルに既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="5a7b1-121">つまり、クライアントが**SaveContentsSort**を呼び出した後に、フォルダーの[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出すと、返されたコンテンツテーブルの行が**SaveContentsSort**で設定された順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="5a7b1-122">すべてのメッセージストアプロバイダーが**SaveContentsSort**をサポートしているわけではありません。メッセージストアプロバイダーは、 **SaveContentsSort**メソッドから MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="5a7b1-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5a7b1-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a7b1-123">See also</span></span>



[<span data-ttu-id="5a7b1-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="5a7b1-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="5a7b1-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="5a7b1-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="5a7b1-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5a7b1-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

