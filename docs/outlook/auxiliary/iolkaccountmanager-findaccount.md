---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: プロパティ値でアカウントを検索します。
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428803"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="85a07-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="85a07-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="85a07-104">プロパティ値でアカウントを検索します。</span><span class="sxs-lookup"><span data-stu-id="85a07-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="85a07-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="85a07-105">Quick info</span></span>

<span data-ttu-id="85a07-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="85a07-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="85a07-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85a07-107">Parameters</span></span>

<span data-ttu-id="85a07-108">_dwprop_</span><span class="sxs-lookup"><span data-stu-id="85a07-108">_dwProp_</span></span>
  
> <span data-ttu-id="85a07-109">順番検索するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="85a07-109">[in] The property to search on.</span></span> <span data-ttu-id="85a07-110">[PROP_ACCT_ID](prop_acct_id.md)または[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)である必要があります。</span><span class="sxs-lookup"><span data-stu-id="85a07-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="85a07-111">_pvar_</span><span class="sxs-lookup"><span data-stu-id="85a07-111">_pVar_</span></span>
  
> <span data-ttu-id="85a07-112">順番一致する値を指定します。</span><span class="sxs-lookup"><span data-stu-id="85a07-112">[in] The value to match.</span></span>
    
<span data-ttu-id="85a07-113">_ppaccount_</span><span class="sxs-lookup"><span data-stu-id="85a07-113">_ppAccount_</span></span>
  
> <span data-ttu-id="85a07-114">読み上げアカウントが見つかりました。</span><span class="sxs-lookup"><span data-stu-id="85a07-114">[out] The account found.</span></span> <span data-ttu-id="85a07-115">このオブジェクトは、 [IOlkAccount](iolkaccount.md)インターフェイスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="85a07-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="85a07-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="85a07-116">Return values</span></span>

|<span data-ttu-id="85a07-117">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="85a07-117">**HRESULT**</span></span>|<span data-ttu-id="85a07-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="85a07-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85a07-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="85a07-119">S_OK</span></span>  <br/> |<span data-ttu-id="85a07-120">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="85a07-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="85a07-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="85a07-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="85a07-122">指定されたアカウントが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="85a07-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="85a07-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="85a07-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="85a07-124">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="85a07-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="85a07-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="85a07-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="85a07-126">1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="85a07-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85a07-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="85a07-127">See also</span></span>

- [<span data-ttu-id="85a07-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="85a07-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="85a07-129">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="85a07-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="85a07-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="85a07-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)

