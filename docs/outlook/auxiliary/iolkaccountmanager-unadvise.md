---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: 通知のすべてのアカウントのアカウント マネージャーを使用するクライアントの登録を解除します。
ms.openlocfilehash: 0632bc6bd98e218cf323262ea480b020185438f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799478"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="19d78-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="19d78-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="19d78-104">通知のすべてのアカウントのアカウント マネージャーを使用するクライアントの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="19d78-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="19d78-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="19d78-105">Quick info</span></span>

<span data-ttu-id="19d78-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="19d78-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="19d78-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="19d78-107">Parameters</span></span>

<span data-ttu-id="19d78-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="19d78-108">_dwCookie_</span></span>
  
> <span data-ttu-id="19d78-109">[in][IOlkAccountManager::Advise](iolkaccountmanager-advise.md)によって返される cookie です。</span><span class="sxs-lookup"><span data-stu-id="19d78-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="19d78-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="19d78-110">Return values</span></span>

|<span data-ttu-id="19d78-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="19d78-111">**HRESULT**</span></span>|<span data-ttu-id="19d78-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="19d78-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="19d78-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="19d78-113">S_OK</span></span>  <br/> |<span data-ttu-id="19d78-114">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="19d78-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="19d78-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="19d78-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="19d78-116">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="19d78-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="19d78-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="19d78-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="19d78-118">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="19d78-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19d78-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="19d78-119">See also</span></span>

- [<span data-ttu-id="19d78-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="19d78-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="19d78-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="19d78-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)

