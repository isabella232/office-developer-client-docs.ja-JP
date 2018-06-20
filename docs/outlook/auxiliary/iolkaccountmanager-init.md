---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: 使用のアカウント マネージャーを初期化します。
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799466"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="e8434-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="e8434-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="e8434-104">使用のアカウント マネージャーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e8434-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e8434-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e8434-105">Quick info</span></span>

<span data-ttu-id="e8434-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="e8434-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="e8434-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8434-107">Parameters</span></span>

<span data-ttu-id="e8434-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="e8434-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="e8434-109">[in]アカウントのヘルパー機能を提供する[IOlkAccountHelper](iolkaccounthelper.md)インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="e8434-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="e8434-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e8434-110">_dwFlags_</span></span>
  
> <span data-ttu-id="e8434-111">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="e8434-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="e8434-112">**ACCT_INIT_NO_STORES_CHECK** -(IMAP アカウントの場合) などのアカウントが、関連付けられているストアとの同期することを防止します。</span><span class="sxs-lookup"><span data-stu-id="e8434-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="e8434-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** -により、MAPI サービス アカウントと同期します。</span><span class="sxs-lookup"><span data-stu-id="e8434-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
    
   - <span data-ttu-id="e8434-114">**OLK_ACCOUNT_NO_FLAGS** -同期の MAPI サービス アカウントです。</span><span class="sxs-lookup"><span data-stu-id="e8434-114">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e8434-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="e8434-115">Return values</span></span>

|<span data-ttu-id="e8434-116">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="e8434-116">**HRESULT**</span></span>|<span data-ttu-id="e8434-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="e8434-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8434-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e8434-118">S_OK</span></span>  <br/> |<span data-ttu-id="e8434-119">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="e8434-119">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="e8434-120">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="e8434-120">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="e8434-121">**初期化**が既に呼び出されています。</span><span class="sxs-lookup"><span data-stu-id="e8434-121">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="e8434-122">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="e8434-122">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="e8434-123">アカウント管理者に必要なレジストリ設定にアクセスできませんでした。</span><span class="sxs-lookup"><span data-stu-id="e8434-123">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8434-124">備考</span><span class="sxs-lookup"><span data-stu-id="e8434-124">Remarks</span></span>

<span data-ttu-id="e8434-125">クライアントは、アカウント マネージャーを使用してアカウントにアクセスしたり、通知を設定する前にアカウントを初期化するために**IOlkAccountManager::Init**マネージャーを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8434-125">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="e8434-126">Outlook は起動時にアカウントを使用して MAPI サービスを自動的に同期をするため、同期するのには特定の原因がない限り、 **ACCT_INIT_NOSYNCH_MAPI_ACCTS**を使用します。</span><span class="sxs-lookup"><span data-stu-id="e8434-126">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8434-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8434-127">See also</span></span>

- [<span data-ttu-id="e8434-128">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="e8434-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

