---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: 指定したカテゴリのアカウントの順序を変更します。
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422860"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="46ae6-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="46ae6-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="46ae6-104">指定したカテゴリのアカウントの順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="46ae6-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="46ae6-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="46ae6-105">Quick info</span></span>

<span data-ttu-id="46ae6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="46ae6-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="46ae6-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="46ae6-107">Parameters</span></span>

<span data-ttu-id="46ae6-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="46ae6-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="46ae6-109">[in]順序を設定するカテゴリ クラス ID。</span><span class="sxs-lookup"><span data-stu-id="46ae6-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="46ae6-110">この値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="46ae6-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="46ae6-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="46ae6-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="46ae6-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="46ae6-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="46ae6-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="46ae6-113">_cAccts_</span></span>
  
> <span data-ttu-id="46ae6-114">[in]アカウントの数。</span><span class="sxs-lookup"><span data-stu-id="46ae6-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="46ae6-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="46ae6-115">_rgAccts_</span></span>
  
> <span data-ttu-id="46ae6-116">[in]アカウントの ID の配列。</span><span class="sxs-lookup"><span data-stu-id="46ae6-116">[in] An array of account IDs.</span></span> <span data-ttu-id="46ae6-117">配列のサイズは  _cAccts です_。</span><span class="sxs-lookup"><span data-stu-id="46ae6-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="46ae6-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="46ae6-118">Return values</span></span>

|<span data-ttu-id="46ae6-119">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="46ae6-119">**HRESULT**</span></span>|<span data-ttu-id="46ae6-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="46ae6-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46ae6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="46ae6-121">S_OK</span></span>  <br/> |<span data-ttu-id="46ae6-122">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="46ae6-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="46ae6-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="46ae6-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="46ae6-124">新しい並べ替え順序のアカウント数は、古い並べ替え順序とは異なります。</span><span class="sxs-lookup"><span data-stu-id="46ae6-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="46ae6-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="46ae6-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="46ae6-126">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="46ae6-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="46ae6-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="46ae6-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="46ae6-128">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="46ae6-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46ae6-129">注釈</span><span class="sxs-lookup"><span data-stu-id="46ae6-129">Remarks</span></span>

<span data-ttu-id="46ae6-130">呼び出し元は、配列ポインター  _prgAccts_ および  _prgAccts_ が指す配列のメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="46ae6-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46ae6-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="46ae6-131">See also</span></span>

- [<span data-ttu-id="46ae6-132">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="46ae6-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="46ae6-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="46ae6-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

