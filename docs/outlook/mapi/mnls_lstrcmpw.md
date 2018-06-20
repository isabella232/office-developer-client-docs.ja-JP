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
ms.openlocfilehash: 8ffd3c8337edcd96af6c3c4e425d274b21fee9f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801644"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="79092-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="79092-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="79092-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79092-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79092-105">2 つの Unicode 文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="79092-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="79092-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="79092-106">Parameters</span></span>

 <span data-ttu-id="79092-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="79092-107">_lpString1_</span></span>
  
> <span data-ttu-id="79092-108">[in]比較する最初の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="79092-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="79092-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="79092-109">_lpString2_</span></span>
  
> <span data-ttu-id="79092-110">[in]比較する 2 番目の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="79092-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79092-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="79092-111">Return value</span></span>

<span data-ttu-id="79092-112">CSTR_EQUAL を除く**MNLS_CompareStringW**に同等の呼び出しの値を返します。</span><span class="sxs-lookup"><span data-stu-id="79092-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="79092-113">備考</span><span class="sxs-lookup"><span data-stu-id="79092-113">Remarks</span></span>

 <span data-ttu-id="79092-114">_MNLS_lstrcmpW_ GetUserDefaultLCID、フラグ、0 のロケールで[MNLS_CompareStringW](mnls_comparestringw.md)を呼び出すことによって比較を実行して cch1 と cch2 の場合は-1 です。</span><span class="sxs-lookup"><span data-stu-id="79092-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79092-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="79092-115">See also</span></span>



[<span data-ttu-id="79092-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="79092-116">GetUserDefaultLCID</span></span>](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

