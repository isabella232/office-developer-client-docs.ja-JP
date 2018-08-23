---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: 指定したアカウントへの変更がクライアントに通知します。
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799489"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="f38ec-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="f38ec-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="f38ec-104">指定したアカウントへの変更がクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="f38ec-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f38ec-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f38ec-105">Quick info</span></span>

<span data-ttu-id="f38ec-106">[IOlkAccountNotify](iolkaccountnotify.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f38ec-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="f38ec-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f38ec-107">Parameters</span></span>

<span data-ttu-id="f38ec-108">_dwNotify_</span><span class="sxs-lookup"><span data-stu-id="f38ec-108">_dwNotify_</span></span>
  
> <span data-ttu-id="f38ec-109">[in]通知の種類です。</span><span class="sxs-lookup"><span data-stu-id="f38ec-109">[in] The type of notification.</span></span> <span data-ttu-id="f38ec-110">値は、次のいずれかする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f38ec-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="f38ec-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="f38ec-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="f38ec-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="f38ec-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="f38ec-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="f38ec-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="f38ec-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="f38ec-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="f38ec-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="f38ec-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="f38ec-116">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="f38ec-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="f38ec-117">[in]作成されており、変更すると、アカウントのアカウント ID は、削除、または削除済みです。</span><span class="sxs-lookup"><span data-stu-id="f38ec-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="f38ec-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="f38ec-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="f38ec-119">[in]使用されません。</span><span class="sxs-lookup"><span data-stu-id="f38ec-119">[in] Not used.</span></span> <span data-ttu-id="f38ec-120">OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。</span><span class="sxs-lookup"><span data-stu-id="f38ec-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f38ec-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="f38ec-121">Return values</span></span>

<span data-ttu-id="f38ec-122">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="f38ec-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f38ec-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f38ec-123">See also</span></span>

- [<span data-ttu-id="f38ec-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="f38ec-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="f38ec-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="f38ec-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

