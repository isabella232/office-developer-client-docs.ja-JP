---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: 指定したアカウントのプロパティの値を取得します。
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799416"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="e0621-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="e0621-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="e0621-104">指定したアカウントのプロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e0621-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e0621-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e0621-105">Quick info</span></span>

<span data-ttu-id="e0621-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0621-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="e0621-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e0621-107">Parameters</span></span>

<span data-ttu-id="e0621-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="e0621-108">_dwProp_</span></span>
  
> <span data-ttu-id="e0621-109">[in]取得するアカウントのプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="e0621-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="e0621-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="e0621-110">_pVar_</span></span>
  
> <span data-ttu-id="e0621-111">[out]指定したプロパティの値です。</span><span class="sxs-lookup"><span data-stu-id="e0621-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e0621-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="e0621-112">Return values</span></span>

|<span data-ttu-id="e0621-113">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="e0621-113">**HRESULT**</span></span>|<span data-ttu-id="e0621-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0621-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0621-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0621-115">S_OK</span></span>  <br/> |<span data-ttu-id="e0621-116">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="e0621-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="e0621-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e0621-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="e0621-118">指定したアカウントのプロパティが見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="e0621-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="e0621-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e0621-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="e0621-120">プロパティの無効なタグが指定されています。</span><span class="sxs-lookup"><span data-stu-id="e0621-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0621-121">注釈</span><span class="sxs-lookup"><span data-stu-id="e0621-121">Remarks</span></span>

<span data-ttu-id="e0621-122">アカウントのプロパティの値がバイナリまたは文字列型の場合、このメソッドが返されると、 [IOlkAccount::FreeMemory](iolkaccount-freememory.md)を使用して、 *pVar*を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0621-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0621-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="e0621-123">See also</span></span>

- [<span data-ttu-id="e0621-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="e0621-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="e0621-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="e0621-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="e0621-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="e0621-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

