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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1f79265c4356747e64aa8102dd4486db229baf5a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579663"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="c6de2-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="c6de2-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="c6de2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6de2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6de2-105">フォルダーの内容のテーブルの既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="c6de2-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c6de2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c6de2-106">Parameters</span></span>

 <span data-ttu-id="c6de2-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="c6de2-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="c6de2-108">[in]既定の並べ替え順序を含む[SSortOrderSet](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c6de2-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="c6de2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c6de2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c6de2-110">[in]既定の並べ替え順序を設定する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c6de2-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="c6de2-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c6de2-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c6de2-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="c6de2-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="c6de2-113">既定の並べ替え順序を設定は、指定されたフォルダーとそのすべてのサブフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="c6de2-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c6de2-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c6de2-114">Return value</span></span>

<span data-ttu-id="c6de2-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6de2-115">S_OK</span></span> 
  
> <span data-ttu-id="c6de2-116">並べ替え順序が正しく保存されました。</span><span class="sxs-lookup"><span data-stu-id="c6de2-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="c6de2-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c6de2-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c6de2-118">メッセージ ストア プロバイダーでは、そのフォルダーの内容のテーブルの並べ替え順序を保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="c6de2-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6de2-119">注釈</span><span class="sxs-lookup"><span data-stu-id="c6de2-119">Remarks</span></span>

<span data-ttu-id="c6de2-120">**IMAPIFolder::SaveContentsSort**メソッドは、フォルダーの内容のテーブルの既定の並べ替え順序を確立します。</span><span class="sxs-lookup"><span data-stu-id="c6de2-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="c6de2-121">**SaveContentsSort**コードの呼び出しの後、クライアントがフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出すと、返されるコンテンツ テーブル内の行は**SaveContentsSort**によって確立された順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6de2-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="c6de2-122">すべてのメッセージ ストア プロバイダーをサポートして**SaveContentsSort**。メッセージ ストア プロバイダーは、 **SaveContentsSort**メソッドから MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="c6de2-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6de2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6de2-123">See also</span></span>



[<span data-ttu-id="c6de2-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="c6de2-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="c6de2-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="c6de2-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="c6de2-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c6de2-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

