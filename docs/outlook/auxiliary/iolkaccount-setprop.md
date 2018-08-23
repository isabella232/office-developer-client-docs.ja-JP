---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: 指定したアカウントのプロパティの値を設定します。
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799433"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="d174c-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="d174c-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="d174c-104">指定したアカウントのプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d174c-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d174c-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d174c-105">Quick info</span></span>

<span data-ttu-id="d174c-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d174c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="d174c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d174c-107">Parameters</span></span>

<span data-ttu-id="d174c-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="d174c-108">_dwProp_</span></span>
  
> <span data-ttu-id="d174c-109">[in]設定するアカウントのプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="d174c-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="d174c-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="d174c-110">_pVar_</span></span>
  
> <span data-ttu-id="d174c-111">[in]指定したプロパティの値です。</span><span class="sxs-lookup"><span data-stu-id="d174c-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d174c-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="d174c-112">Return values</span></span>

|<span data-ttu-id="d174c-113">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="d174c-113">**HRESULT**</span></span>|<span data-ttu-id="d174c-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="d174c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d174c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d174c-115">S_OK</span></span>  <br/> |<span data-ttu-id="d174c-116">メソッドの呼び出しに成功しました。</span><span class="sxs-lookup"><span data-stu-id="d174c-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="d174c-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d174c-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="d174c-118">プロパティの無効なタグが指定されました。</span><span class="sxs-lookup"><span data-stu-id="d174c-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d174c-119">注釈</span><span class="sxs-lookup"><span data-stu-id="d174c-119">Remarks</span></span>

<span data-ttu-id="d174c-120">[IOlkAccount::SaveChanges](iolkaccount-savechanges.md)を使用して、アカウントのプロパティの値に変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="d174c-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d174c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="d174c-121">See also</span></span>

- [<span data-ttu-id="d174c-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="d174c-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="d174c-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="d174c-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

