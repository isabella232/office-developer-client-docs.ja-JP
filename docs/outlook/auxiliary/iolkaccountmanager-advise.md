---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: クライアントをすべてのアカウントに関する通知のアカウント マネージャーに登録します。
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799462"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="a4d54-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="a4d54-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="a4d54-104">クライアントをすべてのアカウントに関する通知のアカウント マネージャーに登録します。</span><span class="sxs-lookup"><span data-stu-id="a4d54-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a4d54-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a4d54-105">Quick info</span></span>

<span data-ttu-id="a4d54-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="a4d54-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="a4d54-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a4d54-107">Parameters</span></span>

<span data-ttu-id="a4d54-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="a4d54-108">_pNotify_</span></span>
  
> <span data-ttu-id="a4d54-109">[in]クライアントに通知を送信するのには、アカウント マネージャーを使用する[IOlkAccountNotify](iolkaccountnotify.md)インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="a4d54-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="a4d54-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="a4d54-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="a4d54-111">[out][IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)は、アカウントの登録を削除するときに使用する cookie です。</span><span class="sxs-lookup"><span data-stu-id="a4d54-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a4d54-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="a4d54-112">Return values</span></span>

|<span data-ttu-id="a4d54-113">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="a4d54-113">**HRESULT**</span></span>|<span data-ttu-id="a4d54-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="a4d54-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4d54-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4d54-115">S_OK</span></span>  <br/> |<span data-ttu-id="a4d54-116">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="a4d54-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="a4d54-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a4d54-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="a4d54-118">無効な引数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="a4d54-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="a4d54-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="a4d54-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="a4d54-120">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="a4d54-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4d54-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="a4d54-121">See also</span></span>

- [<span data-ttu-id="a4d54-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="a4d54-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="a4d54-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a4d54-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

