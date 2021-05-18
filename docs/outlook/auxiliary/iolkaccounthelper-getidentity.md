---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: アカウントのプロファイル名を取得します。
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322107"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="6cacf-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="6cacf-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="6cacf-104">アカウントのプロファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="6cacf-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6cacf-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="6cacf-105">Quick info</span></span>

<span data-ttu-id="6cacf-106">[「IOlkAccountHelper」を参照してください](iolkaccounthelper.md)。</span><span class="sxs-lookup"><span data-stu-id="6cacf-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="6cacf-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6cacf-107">Parameters</span></span>

<span data-ttu-id="6cacf-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="6cacf-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="6cacf-109">[in][out]プロファイル名。</span><span class="sxs-lookup"><span data-stu-id="6cacf-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="6cacf-110">_pcch_</span><span class="sxs-lookup"><span data-stu-id="6cacf-110">_pcch_</span></span>
  
> <span data-ttu-id="6cacf-111">[in][out]このメソッドを呼び出す際に、割り当てられた  _pwszIdentity_ のサイズ (文字数) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6cacf-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="6cacf-112">返された場合、返されるプロファイル名の実際の長さ (0 終端文字を含む) が含まれる。</span><span class="sxs-lookup"><span data-stu-id="6cacf-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6cacf-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="6cacf-113">Return values</span></span>

|<span data-ttu-id="6cacf-114">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="6cacf-114">**HRESULT**</span></span>|<span data-ttu-id="6cacf-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6cacf-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6cacf-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6cacf-116">S_OK</span></span>  <br/> |<span data-ttu-id="6cacf-117">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="6cacf-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="6cacf-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="6cacf-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="6cacf-119">返されるプロファイル名は  _、pwszIdentity_ のサイズよりも長くなります。</span><span class="sxs-lookup"><span data-stu-id="6cacf-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="6cacf-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6cacf-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="6cacf-121">_pcch は_ NULL です。</span><span class="sxs-lookup"><span data-stu-id="6cacf-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cacf-122">注釈</span><span class="sxs-lookup"><span data-stu-id="6cacf-122">Remarks</span></span>

<span data-ttu-id="6cacf-123">_pwszIdentity が_ 小さすぎてプロファイル名を保持できない場合、戻り値に設定され _、pcch_ は _pwszIdentity_ に必要なサイズを指します。</span><span class="sxs-lookup"><span data-stu-id="6cacf-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6cacf-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="6cacf-124">See also</span></span>

- [<span data-ttu-id="6cacf-125">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="6cacf-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="6cacf-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="6cacf-126">PidTagProfileName</span></span>](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

