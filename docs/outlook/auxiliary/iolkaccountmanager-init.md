---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: 使用するアカウント マネージャーを初期化します。
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322037"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="f34d0-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="f34d0-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="f34d0-104">使用するアカウント マネージャーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f34d0-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f34d0-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f34d0-105">Quick info</span></span>

<span data-ttu-id="f34d0-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f34d0-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="f34d0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f34d0-107">Parameters</span></span>

<span data-ttu-id="f34d0-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="f34d0-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="f34d0-109">[in]アカウント [ヘルパー機能を提供する IOlkAccountHelper](iolkaccounthelper.md) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="f34d0-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="f34d0-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="f34d0-110">_dwFlags_</span></span>
  
> <span data-ttu-id="f34d0-111">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="f34d0-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="f34d0-112">**ACCT_INIT_NO_STORES_CHECK** —アカウント (IMAP アカウントなど) が関連付けられたストアと同期しなからせない。</span><span class="sxs-lookup"><span data-stu-id="f34d0-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="f34d0-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —MAPI サービスとアカウントの同期を防止します。</span><span class="sxs-lookup"><span data-stu-id="f34d0-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="f34d0-114">**ACCT_INIT_NO_NOTIFICATIONS** —アカウント マネージャーが他のアプリケーション用のブロードキャスト メッセージを傍受することを防止します。</span><span class="sxs-lookup"><span data-stu-id="f34d0-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="f34d0-115">**OLK_ACCOUNT_NO_FLAGS** —MAPI サービスをアカウントと同期します。</span><span class="sxs-lookup"><span data-stu-id="f34d0-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f34d0-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="f34d0-116">Return values</span></span>

|<span data-ttu-id="f34d0-117">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="f34d0-117">**HRESULT**</span></span>|<span data-ttu-id="f34d0-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="f34d0-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f34d0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f34d0-119">S_OK</span></span>  <br/> |<span data-ttu-id="f34d0-120">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="f34d0-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="f34d0-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f34d0-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="f34d0-122">**Init** は既に呼び出されています。</span><span class="sxs-lookup"><span data-stu-id="f34d0-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="f34d0-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="f34d0-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="f34d0-124">アカウント マネージャーは、必要なレジストリ設定にアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="f34d0-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f34d0-125">注釈</span><span class="sxs-lookup"><span data-stu-id="f34d0-125">Remarks</span></span>

<span data-ttu-id="f34d0-126">アカウント マネージャーを使用してアカウントにアクセスするか、通知を設定する前に、クライアントは **IOlkAccountManager::Init** を呼び出してアカウント マネージャーを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f34d0-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="f34d0-127">MAPI サービスOutlook起動時にアカウントと自動的に同期する場合は、特定の同期 **ACCT_INIT_NOSYNCH_MAPI_ACCTS** を使用します。</span><span class="sxs-lookup"><span data-stu-id="f34d0-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f34d0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="f34d0-128">See also</span></span>

- [<span data-ttu-id="f34d0-129">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="f34d0-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

