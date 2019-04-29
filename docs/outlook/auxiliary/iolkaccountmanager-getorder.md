---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: 指定されたアカウントのカテゴリの順序を取得します。
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424624"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="3a714-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="3a714-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="3a714-104">指定されたアカウントのカテゴリの順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="3a714-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3a714-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3a714-105">Quick info</span></span>

<span data-ttu-id="3a714-106">[IOlkAccountManager](iolkaccountmanager.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3a714-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="3a714-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3a714-107">Parameters</span></span>

<span data-ttu-id="3a714-108">_pclsidcategory_</span><span class="sxs-lookup"><span data-stu-id="3a714-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="3a714-109">順番注文を取得するカテゴリクラス ID。</span><span class="sxs-lookup"><span data-stu-id="3a714-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="3a714-110">値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a714-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="3a714-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="3a714-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="3a714-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="3a714-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="3a714-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="3a714-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="3a714-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="3a714-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="3a714-115">読み上げアカウントの数。</span><span class="sxs-lookup"><span data-stu-id="3a714-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="3a714-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="3a714-116">_prgAccts_</span></span>
  
> <span data-ttu-id="3a714-117">読み上げアカウントの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3a714-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="3a714-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="3a714-118">Return values</span></span>

|<span data-ttu-id="3a714-119">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="3a714-119">**HRESULT**</span></span>|<span data-ttu-id="3a714-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="3a714-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a714-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a714-121">S_OK</span></span>  <br/> |<span data-ttu-id="3a714-122">呼び出しが成功した</span><span class="sxs-lookup"><span data-stu-id="3a714-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="3a714-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3a714-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="3a714-124">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="3a714-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="3a714-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="3a714-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="3a714-126">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="3a714-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a714-127">注釈</span><span class="sxs-lookup"><span data-stu-id="3a714-127">Remarks</span></span>

<span data-ttu-id="3a714-128">このメソッドを呼び出す前に、呼び出し元は配列ポインターのみを割り当てますが、 *prgAccts*は*prgAccts*ポイントの配列のメモリを割り当てません。</span><span class="sxs-lookup"><span data-stu-id="3a714-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="3a714-129">このメソッドが返された後、呼び出し元は[IOlkAccountManager:: FreeMemory](iolkaccountmanager-freememory.md)を使用して、 *prgAccts*に割り当てられているメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a714-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a714-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a714-130">See also</span></span>

- [<span data-ttu-id="3a714-131">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="3a714-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="3a714-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="3a714-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

