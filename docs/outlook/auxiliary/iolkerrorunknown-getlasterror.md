---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: 指定したエラーのメッセージ文字列を取得します。
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431702"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="1a5be-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1a5be-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="1a5be-104">指定したエラーのメッセージ文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a5be-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1a5be-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="1a5be-105">Quick info</span></span>

<span data-ttu-id="1a5be-106">[「IOlkErrorUnknown」を参照してください](iolkerrorunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="1a5be-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="1a5be-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1a5be-107">Parameters</span></span>

<span data-ttu-id="1a5be-108">_hr_</span><span class="sxs-lookup"><span data-stu-id="1a5be-108">_hr_</span></span>
  
> <span data-ttu-id="1a5be-109">[in]参照するエラー コード。</span><span class="sxs-lookup"><span data-stu-id="1a5be-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="1a5be-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="1a5be-110">_ppwszError_</span></span>
  
> <span data-ttu-id="1a5be-111">[out]hr に対応  *するエラー*  メッセージです。</span><span class="sxs-lookup"><span data-stu-id="1a5be-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="1a5be-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="1a5be-112">Return values</span></span>

|<span data-ttu-id="1a5be-113">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="1a5be-113">**HRESULT**</span></span>|<span data-ttu-id="1a5be-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="1a5be-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a5be-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a5be-115">S_OK</span></span>  <br/> |<span data-ttu-id="1a5be-116">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="1a5be-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="1a5be-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1a5be-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="1a5be-118">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="1a5be-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a5be-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a5be-119">See also</span></span>

- [<span data-ttu-id="1a5be-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="1a5be-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

