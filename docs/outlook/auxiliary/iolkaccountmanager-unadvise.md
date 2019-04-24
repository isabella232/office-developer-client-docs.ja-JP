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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322009"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="a2b34-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a2b34-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="a2b34-104">すべてのアカウントの通知について、アカウントマネージャーでクライアントの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="a2b34-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a2b34-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a2b34-105">Quick info</span></span>

<span data-ttu-id="a2b34-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="a2b34-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="a2b34-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a2b34-107">Parameters</span></span>

<span data-ttu-id="a2b34-108">_dwcookie_</span><span class="sxs-lookup"><span data-stu-id="a2b34-108">_dwCookie_</span></span>
  
> <span data-ttu-id="a2b34-109">順番[IOlkAccountManager:: アドバイズ](iolkaccountmanager-advise.md)によって返される cookie。</span><span class="sxs-lookup"><span data-stu-id="a2b34-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a2b34-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="a2b34-110">Return values</span></span>

|<span data-ttu-id="a2b34-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="a2b34-111">**HRESULT**</span></span>|<span data-ttu-id="a2b34-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="a2b34-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2b34-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2b34-113">S_OK</span></span>  <br/> |<span data-ttu-id="a2b34-114">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="a2b34-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="a2b34-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a2b34-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="a2b34-116">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="a2b34-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="a2b34-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="a2b34-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="a2b34-118">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="a2b34-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2b34-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2b34-119">See also</span></span>

- [<span data-ttu-id="a2b34-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="a2b34-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="a2b34-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="a2b34-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

