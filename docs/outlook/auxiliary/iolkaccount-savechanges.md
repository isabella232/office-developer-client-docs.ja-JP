---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: レジストリ ストアに書き込み、アカウント オブジェクトに対する変更をコミットします。
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425835"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="df149-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="df149-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="df149-104">レジストリ ストアに書き込み、アカウント オブジェクトに対する変更をコミットします。</span><span class="sxs-lookup"><span data-stu-id="df149-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="df149-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="df149-105">Quick info</span></span>

<span data-ttu-id="df149-106">[「IOlkAccount」を参照してください](iolkaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="df149-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="df149-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="df149-107">Parameters</span></span>

<span data-ttu-id="df149-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="df149-108">_dwFlags_</span></span>
  
> <span data-ttu-id="df149-109">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="df149-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="df149-110">OLK_ACCOUNT_NO_FLAGSは、サポートされている唯一の値です。</span><span class="sxs-lookup"><span data-stu-id="df149-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="df149-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="df149-111">Return values</span></span>

|<span data-ttu-id="df149-112">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="df149-112">**HRESULT**</span></span>|<span data-ttu-id="df149-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="df149-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df149-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="df149-114">S_OK</span></span>  <br/> |<span data-ttu-id="df149-115">メソッドが成功しました。</span><span class="sxs-lookup"><span data-stu-id="df149-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="df149-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="df149-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="df149-117">指定したアカウントが見当たらされません。</span><span class="sxs-lookup"><span data-stu-id="df149-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="df149-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="df149-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="df149-119">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="df149-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df149-120">注釈</span><span class="sxs-lookup"><span data-stu-id="df149-120">Remarks</span></span>

<span data-ttu-id="df149-121">[IOlkAccount::SetProp](iolkaccount-setprop.md)を使用してアカウント プロパティの値を変更した後 **、IOlkAccount::SaveChanges** を使用して、そのような変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="df149-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df149-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="df149-122">See also</span></span>

- [<span data-ttu-id="df149-123">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="df149-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="df149-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="df149-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)

