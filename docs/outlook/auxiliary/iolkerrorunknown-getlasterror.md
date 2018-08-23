---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: 指定されたエラー メッセージ文字列を取得します。
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799497"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="800b7-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="800b7-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="800b7-104">指定されたエラー メッセージ文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="800b7-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="800b7-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="800b7-105">Quick info</span></span>

<span data-ttu-id="800b7-106">[IOlkErrorUnknown](iolkerrorunknown.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="800b7-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="800b7-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="800b7-107">Parameters</span></span>

<span data-ttu-id="800b7-108">_hr_</span><span class="sxs-lookup"><span data-stu-id="800b7-108">_hr_</span></span>
  
> <span data-ttu-id="800b7-109">[in]参照するエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="800b7-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="800b7-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="800b7-110">_ppwszError_</span></span>
  
> <span data-ttu-id="800b7-111">[out]対応するエラー メッセージに*hr* 。</span><span class="sxs-lookup"><span data-stu-id="800b7-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="800b7-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="800b7-112">Return values</span></span>

|<span data-ttu-id="800b7-113">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="800b7-113">**HRESULT**</span></span>|<span data-ttu-id="800b7-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="800b7-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="800b7-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="800b7-115">S_OK</span></span>  <br/> |<span data-ttu-id="800b7-116">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="800b7-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="800b7-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="800b7-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="800b7-118">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="800b7-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="800b7-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="800b7-119">See also</span></span>

- [<span data-ttu-id="800b7-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="800b7-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

