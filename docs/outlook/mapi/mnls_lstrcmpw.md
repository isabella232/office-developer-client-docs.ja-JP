---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: '最終更新日: 2012 年 6 月 18 日'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356841"
---
# <a name="mnls_lstrcmpw"></a><span data-ttu-id="e8849-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="e8849-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="e8849-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8849-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8849-105">2 つの Unicode 文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="e8849-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="e8849-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8849-106">Parameters</span></span>

 <span data-ttu-id="e8849-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="e8849-107">_lpString1_</span></span>
  
> <span data-ttu-id="e8849-108">[in]比較する最初の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8849-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="e8849-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="e8849-109">_lpString2_</span></span>
  
> <span data-ttu-id="e8849-110">[in]比較する 2 番目の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e8849-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e8849-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="e8849-111">Return value</span></span>

<span data-ttu-id="e8849-112">呼び出しと同等の呼び出しに対して説明されている値を **返MNLS_CompareStringWを** 除CSTR_EQUAL。</span><span class="sxs-lookup"><span data-stu-id="e8849-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8849-113">注釈</span><span class="sxs-lookup"><span data-stu-id="e8849-113">Remarks</span></span>

 <span data-ttu-id="e8849-114">_MNLS_lstrcmpW_ は、getUserDefaultLCID [の](mnls_comparestringw.md) ロケールで MNLS_CompareStringW を呼び出し、フラグに 0、cch1 と cch2 の場合は -1 を呼び出して比較を実行します。</span><span class="sxs-lookup"><span data-stu-id="e8849-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8849-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e8849-115">See also</span></span>



[<span data-ttu-id="e8849-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="e8849-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

