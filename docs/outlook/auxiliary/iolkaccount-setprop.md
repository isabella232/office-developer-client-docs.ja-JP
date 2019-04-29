---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: 指定された account プロパティの値を設定します。
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431989"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="99a4a-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="99a4a-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="99a4a-104">指定された account プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="99a4a-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="99a4a-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="99a4a-105">Quick info</span></span>

<span data-ttu-id="99a4a-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99a4a-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="99a4a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="99a4a-107">Parameters</span></span>

<span data-ttu-id="99a4a-108">_dwprop_</span><span class="sxs-lookup"><span data-stu-id="99a4a-108">_dwProp_</span></span>
  
> <span data-ttu-id="99a4a-109">順番設定する account プロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="99a4a-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="99a4a-110">_pvar_</span><span class="sxs-lookup"><span data-stu-id="99a4a-110">_pVar_</span></span>
  
> <span data-ttu-id="99a4a-111">順番指定したプロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="99a4a-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="99a4a-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="99a4a-112">Return values</span></span>

|<span data-ttu-id="99a4a-113">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="99a4a-113">**HRESULT**</span></span>|<span data-ttu-id="99a4a-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="99a4a-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="99a4a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="99a4a-115">S_OK</span></span>  <br/> |<span data-ttu-id="99a4a-116">メソッドの呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="99a4a-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="99a4a-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="99a4a-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="99a4a-118">無効なプロパティタグが指定されました。</span><span class="sxs-lookup"><span data-stu-id="99a4a-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99a4a-119">注釈</span><span class="sxs-lookup"><span data-stu-id="99a4a-119">Remarks</span></span>

<span data-ttu-id="99a4a-120">[IOlkAccount:: SaveChanges](iolkaccount-savechanges.md)を使用して、アカウントプロパティの値に対する変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="99a4a-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99a4a-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="99a4a-121">See also</span></span>

- [<span data-ttu-id="99a4a-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="99a4a-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="99a4a-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="99a4a-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

