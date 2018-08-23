---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: アカウントの指定したカテゴリの順序を変更します。
ms.openlocfilehash: fcb27404471c9b551320027b0ed6979926ad3d58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799472"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="c2266-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="c2266-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="c2266-104">アカウントの指定したカテゴリの順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="c2266-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c2266-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="c2266-105">Quick info</span></span>

<span data-ttu-id="c2266-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="c2266-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="c2266-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c2266-107">Parameters</span></span>

<span data-ttu-id="c2266-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="c2266-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="c2266-109">[in]順序を設定するカテゴリ クラスの ID です。</span><span class="sxs-lookup"><span data-stu-id="c2266-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="c2266-110">値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2266-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="c2266-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="c2266-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="c2266-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="c2266-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="c2266-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="c2266-113">_cAccts_</span></span>
  
> <span data-ttu-id="c2266-114">[in]アカウントの数です。</span><span class="sxs-lookup"><span data-stu-id="c2266-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="c2266-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="c2266-115">_rgAccts_</span></span>
  
> <span data-ttu-id="c2266-116">[in]アカウント Id の配列。</span><span class="sxs-lookup"><span data-stu-id="c2266-116">[in] An array of account IDs.</span></span> <span data-ttu-id="c2266-117">配列のサイズは、 _cAccts_です。</span><span class="sxs-lookup"><span data-stu-id="c2266-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c2266-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="c2266-118">Return values</span></span>

|<span data-ttu-id="c2266-119">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="c2266-119">**HRESULT**</span></span>|<span data-ttu-id="c2266-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="c2266-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2266-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2266-121">S_OK</span></span>  <br/> |<span data-ttu-id="c2266-122">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="c2266-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="c2266-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="c2266-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="c2266-124">新しい並べ替え順より古い並べ替え順序もアカウントの数が異なるがあります。</span><span class="sxs-lookup"><span data-stu-id="c2266-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="c2266-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c2266-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="c2266-126">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="c2266-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="c2266-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c2266-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="c2266-128">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="c2266-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2266-129">注釈</span><span class="sxs-lookup"><span data-stu-id="c2266-129">Remarks</span></span>

<span data-ttu-id="c2266-130">呼び出し元は、配列のポインターの_prgAccts_である_prgAccts_ポイントの配列にメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c2266-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2266-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2266-131">See also</span></span>

- [<span data-ttu-id="c2266-132">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="c2266-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="c2266-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="c2266-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

