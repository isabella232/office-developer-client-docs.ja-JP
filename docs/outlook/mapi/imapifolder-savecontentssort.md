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
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800492"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="3c572-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="3c572-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="3c572-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c572-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c572-105">フォルダーの内容のテーブルの既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="3c572-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3c572-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3c572-106">Parameters</span></span>

 <span data-ttu-id="3c572-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="3c572-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="3c572-108">[in]既定の並べ替え順序を含む[SSortOrderSet](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3c572-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="3c572-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3c572-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3c572-110">[in]既定の並べ替え順序を設定する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="3c572-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="3c572-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="3c572-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3c572-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="3c572-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="3c572-113">既定の並べ替え順序を設定は、指定されたフォルダーとそのすべてのサブフォルダーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="3c572-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3c572-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3c572-114">Return value</span></span>

<span data-ttu-id="3c572-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c572-115">S_OK</span></span> 
  
> <span data-ttu-id="3c572-116">並べ替え順序が正しく保存されました。</span><span class="sxs-lookup"><span data-stu-id="3c572-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="3c572-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3c572-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3c572-118">メッセージ ストア プロバイダーでは、そのフォルダーの内容のテーブルの並べ替え順序を保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="3c572-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c572-119">備考</span><span class="sxs-lookup"><span data-stu-id="3c572-119">Remarks</span></span>

<span data-ttu-id="3c572-120">**IMAPIFolder::SaveContentsSort**メソッドは、フォルダーの内容のテーブルの既定の並べ替え順序を確立します。</span><span class="sxs-lookup"><span data-stu-id="3c572-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="3c572-121">**SaveContentsSort**コードの呼び出しの後、クライアントがフォルダーの[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出すと、返されるコンテンツ テーブル内の行は**SaveContentsSort**によって確立された順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="3c572-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="3c572-122">すべてのメッセージ ストア プロバイダーをサポートして**SaveContentsSort**。メッセージ ストア プロバイダーは、 **SaveContentsSort**メソッドから MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="3c572-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c572-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c572-123">See also</span></span>



[<span data-ttu-id="3c572-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="3c572-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="3c572-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="3c572-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="3c572-126">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3c572-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

