---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: アカウントの指定したカテゴリの順序を取得します。
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799476"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="8fb99-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="8fb99-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="8fb99-104">アカウントの指定したカテゴリの順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="8fb99-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8fb99-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8fb99-105">Quick info</span></span>

<span data-ttu-id="8fb99-106">[IOlkAccountManager](iolkaccountmanager.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8fb99-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="8fb99-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8fb99-107">Parameters</span></span>

<span data-ttu-id="8fb99-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="8fb99-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="8fb99-109">[in]順序を取得する対象のカテゴリのクラス ID です。</span><span class="sxs-lookup"><span data-stu-id="8fb99-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="8fb99-110">値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fb99-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="8fb99-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="8fb99-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="8fb99-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="8fb99-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="8fb99-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="8fb99-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="8fb99-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="8fb99-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="8fb99-115">[out]アカウントの数です。</span><span class="sxs-lookup"><span data-stu-id="8fb99-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="8fb99-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="8fb99-116">_prgAccts_</span></span>
  
> <span data-ttu-id="8fb99-117">[out]アカウントの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8fb99-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8fb99-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="8fb99-118">Return values</span></span>

|<span data-ttu-id="8fb99-119">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="8fb99-119">**HRESULT**</span></span>|<span data-ttu-id="8fb99-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="8fb99-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8fb99-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="8fb99-121">S_OK</span></span>  <br/> |<span data-ttu-id="8fb99-122">呼び出しに成功しました</span><span class="sxs-lookup"><span data-stu-id="8fb99-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="8fb99-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8fb99-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8fb99-124">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="8fb99-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="8fb99-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8fb99-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="8fb99-126">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="8fb99-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fb99-127">注釈</span><span class="sxs-lookup"><span data-stu-id="8fb99-127">Remarks</span></span>

<span data-ttu-id="8fb99-128">このメソッドを呼び出す前に呼び出し元はである*prgAccts*ポイントの配列ののみ、配列のポインター *prgAccts*がないメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8fb99-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="8fb99-129">このメソッドから制御が戻った後、呼び出し元は、 *prgAccts*に割り当てられたメモリを解放するのには[IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md)を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fb99-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8fb99-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="8fb99-130">See also</span></span>

- [<span data-ttu-id="8fb99-131">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="8fb99-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="8fb99-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="8fb99-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)

