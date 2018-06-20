---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: アカウントのプロファイル名を取得します。
ms.openlocfilehash: 81417282faa9ba0e7ec99990ac78045b54752acb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799468"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="167f5-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="167f5-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="167f5-104">アカウントのプロファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="167f5-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="167f5-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="167f5-105">Quick info</span></span>

<span data-ttu-id="167f5-106">[IOlkAccountHelper](iolkaccounthelper.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="167f5-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="167f5-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="167f5-107">Parameters</span></span>

<span data-ttu-id="167f5-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="167f5-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="167f5-109">[in][out]プロファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="167f5-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="167f5-110">_pcch_</span><span class="sxs-lookup"><span data-stu-id="167f5-110">_pcch_</span></span>
  
> <span data-ttu-id="167f5-111">[in][out]このメソッドを呼び出した時に (文字数) のサイズが割り当てられている_pwszIdentity_が含まれています。</span><span class="sxs-lookup"><span data-stu-id="167f5-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="167f5-112">関数が戻るとき、返されるプロファイル名の 0 終端文字を含めて、実際の長さが含まれています。</span><span class="sxs-lookup"><span data-stu-id="167f5-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="167f5-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="167f5-113">Return values</span></span>

|<span data-ttu-id="167f5-114">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="167f5-114">**HRESULT**</span></span>|<span data-ttu-id="167f5-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="167f5-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="167f5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="167f5-116">S_OK</span></span>  <br/> |<span data-ttu-id="167f5-117">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="167f5-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="167f5-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="167f5-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="167f5-119">返されるプロファイル名は、 _pwszIdentity_のサイズを超えています。</span><span class="sxs-lookup"><span data-stu-id="167f5-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="167f5-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="167f5-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="167f5-121">_pcch_は、NULL です。</span><span class="sxs-lookup"><span data-stu-id="167f5-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="167f5-122">備考</span><span class="sxs-lookup"><span data-stu-id="167f5-122">Remarks</span></span>

<span data-ttu-id="167f5-123">_PwszIdentity_プロファイルの名前を保持するには小さすぎる場合は、返された場合は、設定できませんし、 _pcch_ _pwszIdentity_に必要なサイズをポイントします。</span><span class="sxs-lookup"><span data-stu-id="167f5-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="167f5-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="167f5-124">See also</span></span>

- [<span data-ttu-id="167f5-125">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="167f5-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="167f5-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="167f5-126">PidTagProfileName</span></span>](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

