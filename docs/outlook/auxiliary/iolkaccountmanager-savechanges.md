---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: 指定されたアカウントに変更を保存します。
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799484"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="62642-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="62642-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="62642-104">指定されたアカウントに変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="62642-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="62642-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="62642-105">Quick info</span></span>

<span data-ttu-id="62642-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="62642-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="62642-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="62642-107">Parameters</span></span>

<span data-ttu-id="62642-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="62642-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="62642-109">[in]アカウント ID を保存します。</span><span class="sxs-lookup"><span data-stu-id="62642-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="62642-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="62642-110">_dwFlags_</span></span>
  
> <span data-ttu-id="62642-111">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="62642-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="62642-112">OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。</span><span class="sxs-lookup"><span data-stu-id="62642-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="62642-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="62642-113">Return values</span></span>

|<span data-ttu-id="62642-114">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="62642-114">**HRESULT**</span></span>|<span data-ttu-id="62642-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="62642-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62642-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="62642-116">S_OK</span></span>  <br/> |<span data-ttu-id="62642-117">呼び出しに成功しました</span><span class="sxs-lookup"><span data-stu-id="62642-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="62642-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="62642-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="62642-119">指定されたアカウントが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="62642-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="62642-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="62642-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="62642-121">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="62642-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62642-122">注釈</span><span class="sxs-lookup"><span data-stu-id="62642-122">Remarks</span></span>

<span data-ttu-id="62642-123">[IOlkAccount::SetProp](iolkaccount-setprop.md)を使用してアカウントのプロパティの値を変更した後に、このような変更を保存するのには**IOlkAccountManager::SaveChanges**または[IOlkAccount::SaveChanges](iolkaccount-savechanges.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="62642-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62642-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="62642-124">See also</span></span>

- [<span data-ttu-id="62642-125">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="62642-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="62642-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="62642-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)

