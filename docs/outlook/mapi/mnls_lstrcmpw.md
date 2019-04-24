---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: '最終更新日: 2012 年6月18日'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356841"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="46724-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="46724-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="46724-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46724-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46724-105">2つの Unicode 文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="46724-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="46724-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="46724-106">Parameters</span></span>

 <span data-ttu-id="46724-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="46724-107">_lpString1_</span></span>
  
> <span data-ttu-id="46724-108">順番比較する最初の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="46724-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="46724-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="46724-109">_lpString2_</span></span>
  
> <span data-ttu-id="46724-110">順番比較する2番目の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="46724-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46724-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="46724-111">Return value</span></span>

<span data-ttu-id="46724-112">CSTR_EQUAL 以外の**MNLS_CompareStringW**への同等の呼び出しについて記述されている値を返します。</span><span class="sxs-lookup"><span data-stu-id="46724-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="46724-113">解説</span><span class="sxs-lookup"><span data-stu-id="46724-113">Remarks</span></span>

 <span data-ttu-id="46724-114">_MNLS_lstrcmpW_は、getuserdefaultlcid のロケールで[MNLS_CompareStringW](mnls_comparestringw.md)を呼び出し、フラグに0、cch1 および cch2 に-1 を呼び出して比較を実行します。</span><span class="sxs-lookup"><span data-stu-id="46724-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46724-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="46724-115">See also</span></span>



[<span data-ttu-id="46724-116">getuserdefaultlcid</span><span class="sxs-lookup"><span data-stu-id="46724-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

