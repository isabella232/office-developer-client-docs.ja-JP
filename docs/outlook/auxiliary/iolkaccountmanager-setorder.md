---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: 指定したアカウントのカテゴリの順序を変更します。
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322044"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="b030a-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="b030a-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="b030a-104">指定したアカウントのカテゴリの順序を変更します。</span><span class="sxs-lookup"><span data-stu-id="b030a-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b030a-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b030a-105">Quick info</span></span>

<span data-ttu-id="b030a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b030a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="b030a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b030a-107">Parameters</span></span>

<span data-ttu-id="b030a-108">_pclsidcategory_</span><span class="sxs-lookup"><span data-stu-id="b030a-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="b030a-109">順番順序を設定するカテゴリクラス ID。</span><span class="sxs-lookup"><span data-stu-id="b030a-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="b030a-110">この値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b030a-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="b030a-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="b030a-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="b030a-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="b030a-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="b030a-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="b030a-113">_cAccts_</span></span>
  
> <span data-ttu-id="b030a-114">順番アカウントの数。</span><span class="sxs-lookup"><span data-stu-id="b030a-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="b030a-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="b030a-115">_rgAccts_</span></span>
  
> <span data-ttu-id="b030a-116">順番アカウント id の配列。</span><span class="sxs-lookup"><span data-stu-id="b030a-116">[in] An array of account IDs.</span></span> <span data-ttu-id="b030a-117">配列のサイズは_cAccts_です。</span><span class="sxs-lookup"><span data-stu-id="b030a-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b030a-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="b030a-118">Return values</span></span>

|<span data-ttu-id="b030a-119">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="b030a-119">**HRESULT**</span></span>|<span data-ttu-id="b030a-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="b030a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b030a-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b030a-121">S_OK</span></span>  <br/> |<span data-ttu-id="b030a-122">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="b030a-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b030a-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="b030a-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="b030a-124">新しい並べ替え順序には、古い並べ替え順序とは異なる数のアカウントがあります。</span><span class="sxs-lookup"><span data-stu-id="b030a-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="b030a-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b030a-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="b030a-126">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="b030a-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="b030a-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b030a-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b030a-128">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="b030a-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b030a-129">解説</span><span class="sxs-lookup"><span data-stu-id="b030a-129">Remarks</span></span>

<span data-ttu-id="b030a-130">呼び出し元は、配列ポインター _prgAccts_および_prgAccts_がポイントする配列のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b030a-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b030a-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="b030a-131">See also</span></span>

- [<span data-ttu-id="b030a-132">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="b030a-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="b030a-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="b030a-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

