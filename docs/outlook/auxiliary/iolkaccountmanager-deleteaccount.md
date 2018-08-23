---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: 指定したアカウントを削除します。
ms.openlocfilehash: 1c0b246af10dac1af9c61f368d082a92c7b3616a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799470"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="822ab-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="822ab-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="822ab-104">指定したアカウントを削除します。</span><span class="sxs-lookup"><span data-stu-id="822ab-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="822ab-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="822ab-105">Quick info</span></span>

<span data-ttu-id="822ab-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="822ab-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="822ab-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="822ab-107">Parameters</span></span>

<span data-ttu-id="822ab-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="822ab-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="822ab-109">[in]削除するアカウントのアカウント ID です。</span><span class="sxs-lookup"><span data-stu-id="822ab-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="822ab-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="822ab-110">Return values</span></span>

|<span data-ttu-id="822ab-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="822ab-111">**HRESULT**</span></span>|<span data-ttu-id="822ab-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="822ab-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="822ab-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="822ab-113">S_OK</span></span>  <br/> |<span data-ttu-id="822ab-114">呼び出しに成功しました</span><span class="sxs-lookup"><span data-stu-id="822ab-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="822ab-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="822ab-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="822ab-116">指定されたアカウントが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="822ab-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="822ab-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="822ab-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="822ab-118">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="822ab-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="822ab-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="822ab-119">See also</span></span>

- [<span data-ttu-id="822ab-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="822ab-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="822ab-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="822ab-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)

