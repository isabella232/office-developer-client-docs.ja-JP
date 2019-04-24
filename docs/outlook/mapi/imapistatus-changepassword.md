---
title: imapistatuschangepassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328281"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="b66dd-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="b66dd-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="b66dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b66dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b66dd-105">ユーザーインターフェイスを表示せずに、サービスプロバイダーのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="b66dd-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="b66dd-106">このメソッドは、サービスプロバイダーが実装する status オブジェクトで必要に応じてサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b66dd-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b66dd-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b66dd-107">Parameters</span></span>

 <span data-ttu-id="b66dd-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="b66dd-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="b66dd-109">順番古いパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b66dd-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="b66dd-110">_lpnewpass_</span><span class="sxs-lookup"><span data-stu-id="b66dd-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="b66dd-111">順番新しいパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b66dd-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="b66dd-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b66dd-112">_ulFlags_</span></span>
  
> <span data-ttu-id="b66dd-113">順番パスワードの形式を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b66dd-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="b66dd-114">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b66dd-114">The following flag can be set:</span></span>
    
<span data-ttu-id="b66dd-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b66dd-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b66dd-116">パスワードは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="b66dd-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="b66dd-117">MAPI_UNICODE フラグが設定されていない場合、パスワードは ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="b66dd-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b66dd-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="b66dd-118">Return value</span></span>

<span data-ttu-id="b66dd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b66dd-119">S_OK</span></span> 
  
> <span data-ttu-id="b66dd-120">パスワードの変更に成功しました。</span><span class="sxs-lookup"><span data-stu-id="b66dd-120">The password modification was successful.</span></span>
    
<span data-ttu-id="b66dd-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b66dd-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b66dd-122">_lpOldPass_が指す古いパスワードが無効です。</span><span class="sxs-lookup"><span data-stu-id="b66dd-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="b66dd-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b66dd-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b66dd-124">status オブジェクトの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_CHANGE_PASSWORD フラグが設定されていない場合、status オブジェクトはこの操作をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b66dd-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b66dd-125">解説</span><span class="sxs-lookup"><span data-stu-id="b66dd-125">Remarks</span></span>

<span data-ttu-id="b66dd-126">すべてのステータスオブジェクトが**imapistatus:: ChangePassword**メソッドをサポートするわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b66dd-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="b66dd-127">クライアントがパスワードを入力する必要があるサービスプロバイダーのみがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b66dd-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="b66dd-128">MAPI で実装されているステータスオブジェクトは、パスワードの変更操作をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b66dd-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="b66dd-129">**ChangePassword**ユーザーによる操作なしで、プログラムによってパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="b66dd-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b66dd-130">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="b66dd-130">Notes to implementers</span></span>

<span data-ttu-id="b66dd-131">リモートトランスポートプロバイダーは、ここで指定したように**ChangePassword**を実装します。</span><span class="sxs-lookup"><span data-stu-id="b66dd-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="b66dd-132">特別な考慮事項はありません。</span><span class="sxs-lookup"><span data-stu-id="b66dd-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b66dd-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="b66dd-133">See also</span></span>



[<span data-ttu-id="b66dd-134">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b66dd-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="b66dd-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b66dd-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

