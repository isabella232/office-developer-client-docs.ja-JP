---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: アカウントマネージャーにクライアントを登録して、すべてのアカウントに関する通知を行います。
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322198"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="9175c-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="9175c-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="9175c-104">アカウントマネージャーにクライアントを登録して、すべてのアカウントに関する通知を行います。</span><span class="sxs-lookup"><span data-stu-id="9175c-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9175c-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9175c-105">Quick info</span></span>

<span data-ttu-id="9175c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="9175c-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="9175c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9175c-107">Parameters</span></span>

<span data-ttu-id="9175c-108">_pnotify_</span><span class="sxs-lookup"><span data-stu-id="9175c-108">_pNotify_</span></span>
  
> <span data-ttu-id="9175c-109">順番アカウントマネージャーがクライアントに通知を送信するために使用する[IOlkAccountNotify](iolkaccountnotify.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="9175c-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="9175c-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="9175c-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="9175c-111">読み上げ[IOlkAccountManager:: アドバイズ](iolkaccountmanager-unadvise.md)中止は、アカウントの登録を削除するときに使用する cookie です。</span><span class="sxs-lookup"><span data-stu-id="9175c-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="9175c-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="9175c-112">Return values</span></span>

|<span data-ttu-id="9175c-113">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="9175c-113">**HRESULT**</span></span>|<span data-ttu-id="9175c-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="9175c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9175c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="9175c-115">S_OK</span></span>  <br/> |<span data-ttu-id="9175c-116">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="9175c-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="9175c-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9175c-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="9175c-118">無効な引数が指定されています。</span><span class="sxs-lookup"><span data-stu-id="9175c-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="9175c-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="9175c-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="9175c-120">アカウント マネージャーが使用するために初期化されていません。</span><span class="sxs-lookup"><span data-stu-id="9175c-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9175c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="9175c-121">See also</span></span>

- [<span data-ttu-id="9175c-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="9175c-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="9175c-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="9175c-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)

