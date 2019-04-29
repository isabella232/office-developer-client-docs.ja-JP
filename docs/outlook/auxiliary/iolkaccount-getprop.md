---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: 指定されたアカウントのプロパティの値を取得します。
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433739"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="41d43-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="41d43-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="41d43-104">指定されたアカウントのプロパティの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="41d43-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="41d43-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="41d43-105">Quick info</span></span>

<span data-ttu-id="41d43-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41d43-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="41d43-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="41d43-107">Parameters</span></span>

<span data-ttu-id="41d43-108">_dwprop_</span><span class="sxs-lookup"><span data-stu-id="41d43-108">_dwProp_</span></span>
  
> <span data-ttu-id="41d43-109">順番取得する account プロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="41d43-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="41d43-110">_pvar_</span><span class="sxs-lookup"><span data-stu-id="41d43-110">_pVar_</span></span>
  
> <span data-ttu-id="41d43-111">読み上げ指定したプロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="41d43-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="41d43-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="41d43-112">Return values</span></span>

|<span data-ttu-id="41d43-113">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="41d43-113">**HRESULT**</span></span>|<span data-ttu-id="41d43-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="41d43-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41d43-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="41d43-115">S_OK</span></span>  <br/> |<span data-ttu-id="41d43-116">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="41d43-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="41d43-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="41d43-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="41d43-118">指定されたアカウントのプロパティが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="41d43-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="41d43-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="41d43-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="41d43-120">無効なプロパティタグが指定されています。</span><span class="sxs-lookup"><span data-stu-id="41d43-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41d43-121">注釈</span><span class="sxs-lookup"><span data-stu-id="41d43-121">Remarks</span></span>

<span data-ttu-id="41d43-122">このメソッドが返された後、account プロパティの値がバイナリ型または文字列型の場合は、 [IOlkAccount:: FreeMemory](iolkaccount-freememory.md)を使用して*pvar*を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41d43-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41d43-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="41d43-123">See also</span></span>

- [<span data-ttu-id="41d43-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="41d43-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="41d43-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="41d43-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="41d43-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="41d43-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)

