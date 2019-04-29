---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: 指定したアカウントへの変更をクライアントに通知します。
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424568"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="9c668-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="9c668-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="9c668-104">指定したアカウントへの変更をクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="9c668-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9c668-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="9c668-105">Quick info</span></span>

<span data-ttu-id="9c668-106">[IOlkAccountNotify](iolkaccountnotify.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c668-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="9c668-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9c668-107">Parameters</span></span>

<span data-ttu-id="9c668-108">_dwnotify_</span><span class="sxs-lookup"><span data-stu-id="9c668-108">_dwNotify_</span></span>
  
> <span data-ttu-id="9c668-109">順番通知の種類。</span><span class="sxs-lookup"><span data-stu-id="9c668-109">[in] The type of notification.</span></span> <span data-ttu-id="9c668-110">この値は、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c668-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="9c668-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="9c668-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="9c668-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="9c668-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="9c668-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="9c668-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="9c668-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="9c668-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="9c668-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="9c668-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="9c668-116">_dwて tid_</span><span class="sxs-lookup"><span data-stu-id="9c668-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="9c668-117">順番作成、変更、削除、または事前削除されたアカウントのアカウント ID。</span><span class="sxs-lookup"><span data-stu-id="9c668-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="9c668-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="9c668-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="9c668-119">順番使用されません。</span><span class="sxs-lookup"><span data-stu-id="9c668-119">[in] Not used.</span></span> <span data-ttu-id="9c668-120">OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。</span><span class="sxs-lookup"><span data-stu-id="9c668-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="9c668-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="9c668-121">Return values</span></span>

<span data-ttu-id="9c668-122">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="9c668-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c668-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c668-123">See also</span></span>

- [<span data-ttu-id="9c668-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="9c668-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="9c668-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="9c668-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)

