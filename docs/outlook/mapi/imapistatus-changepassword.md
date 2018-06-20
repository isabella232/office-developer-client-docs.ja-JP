---
title: IMAPIStatusChangePassword
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800716"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="b2791-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="b2791-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="b2791-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2791-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2791-105">ユーザー インターフェイスを表示せずには、サービス プロバイダーのパスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="b2791-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="b2791-106">サービス プロバイダーを実装する状態オブジェクトには、このメソッドはサポートされて必要に応じてします。</span><span class="sxs-lookup"><span data-stu-id="b2791-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b2791-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2791-107">Parameters</span></span>

 <span data-ttu-id="b2791-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="b2791-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="b2791-109">[in]古いパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b2791-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="b2791-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="b2791-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="b2791-111">[in]新しいパスワードへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b2791-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="b2791-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2791-112">_ulFlags_</span></span>
  
> <span data-ttu-id="b2791-113">[in]パスワードの形式を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="b2791-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="b2791-114">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b2791-114">The following flag can be set:</span></span>
    
<span data-ttu-id="b2791-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b2791-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b2791-116">パスワードは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="b2791-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="b2791-117">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のパスワードです。</span><span class="sxs-lookup"><span data-stu-id="b2791-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2791-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b2791-118">Return value</span></span>

<span data-ttu-id="b2791-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2791-119">S_OK</span></span> 
  
> <span data-ttu-id="b2791-120">パスワードの変更が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="b2791-120">The password modification was successful.</span></span>
    
<span data-ttu-id="b2791-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b2791-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b2791-122">_LpOldPass_で指定された古いパスワードが正しくありません。</span><span class="sxs-lookup"><span data-stu-id="b2791-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="b2791-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b2791-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="b2791-124">状態オブジェクトは、この操作をサポートしていません状態オブジェクトの**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティに STATUS_CHANGE_PASSWORD フラグがない場合で示される。</span><span class="sxs-lookup"><span data-stu-id="b2791-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2791-125">備考</span><span class="sxs-lookup"><span data-stu-id="b2791-125">Remarks</span></span>

<span data-ttu-id="b2791-126">ステータスのすべてのオブジェクトは、 **IMAPIStatus::ChangePassword**メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b2791-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="b2791-127">クライアントがパスワードの入力を必要とするサービス ・ プロバイダーでのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b2791-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="b2791-128">MAPI が実装している状態のオブジェクトの [なし] は、パスワードの変更操作をサポートします。</span><span class="sxs-lookup"><span data-stu-id="b2791-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="b2791-129">**パスワードの変更**は、ユーザーの介入なしプログラムで、パスワードを変更します。</span><span class="sxs-lookup"><span data-stu-id="b2791-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b2791-130">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="b2791-130">Notes to implementers</span></span>

<span data-ttu-id="b2791-131">リモート トランスポート プロバイダーは、ここで指定されている**パスワードの変更**を実装します。</span><span class="sxs-lookup"><span data-stu-id="b2791-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="b2791-132">特別な考慮事項はありません。</span><span class="sxs-lookup"><span data-stu-id="b2791-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2791-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="b2791-133">See also</span></span>



[<span data-ttu-id="b2791-134">PidTagResourceMethods の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b2791-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="b2791-135">IMAPIStatus: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b2791-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

