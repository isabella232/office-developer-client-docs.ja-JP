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
ms.openlocfilehash: 36e22c60b32242425335b122b66c2c77e376848b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580118"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="920f8-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="920f8-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="920f8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="920f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="920f8-105">2 つの Unicode 文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="920f8-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="920f8-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="920f8-106">Parameters</span></span>

 <span data-ttu-id="920f8-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="920f8-107">_lpString1_</span></span>
  
> <span data-ttu-id="920f8-108">[in]比較する最初の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="920f8-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="920f8-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="920f8-109">_lpString2_</span></span>
  
> <span data-ttu-id="920f8-110">[in]比較する 2 番目の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="920f8-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="920f8-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="920f8-111">Return value</span></span>

<span data-ttu-id="920f8-112">CSTR_EQUAL を除く**MNLS_CompareStringW**に同等の呼び出しの値を返します。</span><span class="sxs-lookup"><span data-stu-id="920f8-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="920f8-113">注釈</span><span class="sxs-lookup"><span data-stu-id="920f8-113">Remarks</span></span>

 <span data-ttu-id="920f8-114">_MNLS_lstrcmpW_ GetUserDefaultLCID、フラグ、0 のロケールで[MNLS_CompareStringW](mnls_comparestringw.md)を呼び出すことによって比較を実行して cch1 と cch2 の場合は-1 です。</span><span class="sxs-lookup"><span data-stu-id="920f8-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="920f8-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="920f8-115">See also</span></span>



[<span data-ttu-id="920f8-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="920f8-116">GetUserDefaultLCID</span></span>](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

