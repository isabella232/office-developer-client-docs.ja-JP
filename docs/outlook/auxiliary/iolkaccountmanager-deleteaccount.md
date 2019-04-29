---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: 指定されたアカウントを削除します。
ms.openlocfilehash: 3e39b7b9af57f64dd124e1bf836db68664709b8c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431240"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="04def-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="04def-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="04def-104">指定されたアカウントを削除します。</span><span class="sxs-lookup"><span data-stu-id="04def-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="04def-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="04def-105">Quick info</span></span>

<span data-ttu-id="04def-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="04def-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="04def-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04def-107">Parameters</span></span>

<span data-ttu-id="04def-108">_dwて tid_</span><span class="sxs-lookup"><span data-stu-id="04def-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="04def-109">順番削除するアカウントのアカウント ID。</span><span class="sxs-lookup"><span data-stu-id="04def-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="04def-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="04def-110">Return values</span></span>

|<span data-ttu-id="04def-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="04def-111">**HRESULT**</span></span>|<span data-ttu-id="04def-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="04def-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04def-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="04def-113">S_OK</span></span>  <br/> |<span data-ttu-id="04def-114">呼び出しが成功した</span><span class="sxs-lookup"><span data-stu-id="04def-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="04def-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="04def-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="04def-116">指定されたアカウントが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="04def-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="04def-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="04def-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="04def-118">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="04def-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04def-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="04def-119">See also</span></span>

- [<span data-ttu-id="04def-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="04def-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="04def-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="04def-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

