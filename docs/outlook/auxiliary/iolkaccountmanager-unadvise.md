---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: すべてのアカウントの通知について、アカウントマネージャーでクライアントの登録を解除します。
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430988"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="fd94d-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="fd94d-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="fd94d-104">すべてのアカウントの通知について、アカウントマネージャーでクライアントの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="fd94d-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="fd94d-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="fd94d-105">Quick info</span></span>

<span data-ttu-id="fd94d-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="fd94d-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="fd94d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fd94d-107">Parameters</span></span>

<span data-ttu-id="fd94d-108">_dwcookie_</span><span class="sxs-lookup"><span data-stu-id="fd94d-108">_dwCookie_</span></span>
  
> <span data-ttu-id="fd94d-109">順番[IOlkAccountManager:: アドバイズ](iolkaccountmanager-advise.md)によって返される cookie。</span><span class="sxs-lookup"><span data-stu-id="fd94d-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fd94d-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="fd94d-110">Return values</span></span>

|<span data-ttu-id="fd94d-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="fd94d-111">**HRESULT**</span></span>|<span data-ttu-id="fd94d-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="fd94d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd94d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd94d-113">S_OK</span></span>  <br/> |<span data-ttu-id="fd94d-114">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="fd94d-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="fd94d-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fd94d-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="fd94d-116">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="fd94d-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="fd94d-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="fd94d-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="fd94d-118">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="fd94d-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd94d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd94d-119">See also</span></span>

- [<span data-ttu-id="fd94d-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="fd94d-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="fd94d-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="fd94d-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

