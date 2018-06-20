---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: プロパティの値によっては、アカウントを検索します。
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799469"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="96da8-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="96da8-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="96da8-104">プロパティの値によっては、アカウントを検索します。</span><span class="sxs-lookup"><span data-stu-id="96da8-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="96da8-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="96da8-105">Quick info</span></span>

<span data-ttu-id="96da8-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="96da8-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="96da8-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="96da8-107">Parameters</span></span>

<span data-ttu-id="96da8-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="96da8-108">_dwProp_</span></span>
  
> <span data-ttu-id="96da8-109">[in]検索するプロパティです。</span><span class="sxs-lookup"><span data-stu-id="96da8-109">[in] The property to search on.</span></span> <span data-ttu-id="96da8-110">[PROP_ACCT_ID](prop_acct_id.md)または[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)である必要があります。</span><span class="sxs-lookup"><span data-stu-id="96da8-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="96da8-111">_pVar_</span><span class="sxs-lookup"><span data-stu-id="96da8-111">_pVar_</span></span>
  
> <span data-ttu-id="96da8-112">[in]一致する値。</span><span class="sxs-lookup"><span data-stu-id="96da8-112">[in] The value to match.</span></span>
    
<span data-ttu-id="96da8-113">_ppAccount_</span><span class="sxs-lookup"><span data-stu-id="96da8-113">_ppAccount_</span></span>
  
> <span data-ttu-id="96da8-114">[out]アカウントは見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="96da8-114">[out] The account found.</span></span> <span data-ttu-id="96da8-115">このオブジェクトは、 [IOlkAccount](iolkaccount.md)インターフェイスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="96da8-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="96da8-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="96da8-116">Return values</span></span>

|<span data-ttu-id="96da8-117">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="96da8-117">**HRESULT**</span></span>|<span data-ttu-id="96da8-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="96da8-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="96da8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="96da8-119">S_OK</span></span>  <br/> |<span data-ttu-id="96da8-120">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="96da8-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="96da8-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="96da8-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="96da8-122">指定されたアカウントが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="96da8-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="96da8-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="96da8-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="96da8-124">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="96da8-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="96da8-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="96da8-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="96da8-126">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="96da8-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96da8-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="96da8-127">See also</span></span>

- [<span data-ttu-id="96da8-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="96da8-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="96da8-129">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="96da8-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="96da8-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="96da8-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

