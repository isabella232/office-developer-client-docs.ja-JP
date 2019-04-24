---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: 使用するアカウントマネージャーを初期化します。
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322037"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="34160-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="34160-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="34160-104">使用するアカウントマネージャーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="34160-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="34160-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="34160-105">Quick info</span></span>

<span data-ttu-id="34160-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="34160-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="34160-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="34160-107">Parameters</span></span>

<span data-ttu-id="34160-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="34160-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="34160-109">順番アカウントヘルパー機能を提供する[IOlkAccountHelper](iolkaccounthelper.md)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="34160-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="34160-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="34160-110">_dwFlags_</span></span>
  
> <span data-ttu-id="34160-111">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="34160-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="34160-112">**ACCT_INIT_NO_STORES_CHECK** —アカウント (IMAP アカウントなど) が関連ストアと同期しないようにします。</span><span class="sxs-lookup"><span data-stu-id="34160-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="34160-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** : MAPI サービスがアカウントと同期できないようにします。</span><span class="sxs-lookup"><span data-stu-id="34160-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="34160-114">**ACCT_INIT_NO_NOTIFICATIONS** —アカウントマネージャーが他のアプリケーションに送信されるブロードキャストメッセージを受信できないようにします。</span><span class="sxs-lookup"><span data-stu-id="34160-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="34160-115">**OLK_ACCOUNT_NO_FLAGS** — MAPI サービスをアカウントと同期します。</span><span class="sxs-lookup"><span data-stu-id="34160-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="34160-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="34160-116">Return values</span></span>

|<span data-ttu-id="34160-117">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="34160-117">**HRESULT**</span></span>|<span data-ttu-id="34160-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="34160-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34160-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="34160-119">S_OK</span></span>  <br/> |<span data-ttu-id="34160-120">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="34160-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="34160-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="34160-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="34160-122">**Init**は既に呼び出されています。</span><span class="sxs-lookup"><span data-stu-id="34160-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="34160-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="34160-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="34160-124">アカウントマネージャーは、必要なレジストリ設定にアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="34160-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34160-125">解説</span><span class="sxs-lookup"><span data-stu-id="34160-125">Remarks</span></span>

<span data-ttu-id="34160-126">アカウントマネージャーを使用してアカウントにアクセスしたり通知を設定したりする前に、クライアントは**IOlkAccountManager:: Init**を呼び出してアカウントマネージャーを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34160-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="34160-127">Outlook は起動時に MAPI サービスをアカウントに自動的に同期するので、同期する具体的な原因がない限り、 **ACCT_INIT_NOSYNCH_MAPI_ACCTS**を使用します。</span><span class="sxs-lookup"><span data-stu-id="34160-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34160-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="34160-128">See also</span></span>

- [<span data-ttu-id="34160-129">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="34160-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

