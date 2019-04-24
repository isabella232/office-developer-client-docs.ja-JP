---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: 指定したアカウントに変更内容を保存します。
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322023"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="8e6b1-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8e6b1-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="8e6b1-104">指定したアカウントに変更内容を保存します。</span><span class="sxs-lookup"><span data-stu-id="8e6b1-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8e6b1-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8e6b1-105">Quick info</span></span>

<span data-ttu-id="8e6b1-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="8e6b1-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="8e6b1-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8e6b1-107">Parameters</span></span>

<span data-ttu-id="8e6b1-108">_dwて tid_</span><span class="sxs-lookup"><span data-stu-id="8e6b1-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="8e6b1-109">順番保存するアカウント ID。</span><span class="sxs-lookup"><span data-stu-id="8e6b1-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="8e6b1-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8e6b1-110">_dwFlags_</span></span>
  
> <span data-ttu-id="8e6b1-111">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="8e6b1-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="8e6b1-112">OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。</span><span class="sxs-lookup"><span data-stu-id="8e6b1-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8e6b1-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="8e6b1-113">Return values</span></span>

|<span data-ttu-id="8e6b1-114">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="8e6b1-114">**HRESULT**</span></span>|<span data-ttu-id="8e6b1-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="8e6b1-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e6b1-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e6b1-116">S_OK</span></span>  <br/> |<span data-ttu-id="8e6b1-117">呼び出しが成功した</span><span class="sxs-lookup"><span data-stu-id="8e6b1-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="8e6b1-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8e6b1-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="8e6b1-119">指定されたアカウントが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="8e6b1-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="8e6b1-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8e6b1-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="8e6b1-121">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="8e6b1-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e6b1-122">解説</span><span class="sxs-lookup"><span data-stu-id="8e6b1-122">Remarks</span></span>

<span data-ttu-id="8e6b1-123">[IOlkAccount:: setprop](iolkaccount-setprop.md)を使用して、account プロパティの値を変更した後、 **IOlkAccountManager:: savechanges**または[IOlkAccount:: savechanges](iolkaccount-savechanges.md)を使用してこれらの変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="8e6b1-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e6b1-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e6b1-124">See also</span></span>

- [<span data-ttu-id="8e6b1-125">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="8e6b1-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="8e6b1-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8e6b1-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

