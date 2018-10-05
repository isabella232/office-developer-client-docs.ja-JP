---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: '最終更新日: 2012 年 2 月 20 日'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396212"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="bd14e-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="bd14e-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="bd14e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd14e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd14e-105">2 つの Unicode 文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="bd14e-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="bd14e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bd14e-106">Parameters</span></span>

 <span data-ttu-id="bd14e-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="bd14e-107">_lcid_</span></span>
  
> <span data-ttu-id="bd14e-108">[in]ロケール識別子です。</span><span class="sxs-lookup"><span data-stu-id="bd14e-108">[in] Locale identifier.</span></span> <span data-ttu-id="bd14e-109">詳細な定義は、[通常](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)の_ロケール_パラメーターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd14e-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="bd14e-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="bd14e-110">_dwFlags_</span></span>
  
> <span data-ttu-id="bd14e-111">[in]大文字と小文字およびアクセント記号を無視するようにフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="bd14e-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="bd14e-112">詳細な定義は、 [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)の_dwCmpFlags_パラメーターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd14e-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="bd14e-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="bd14e-113">_pstr1_</span></span>
  
> <span data-ttu-id="bd14e-114">[in]比較する最初の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bd14e-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="bd14e-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="bd14e-115">_cch1_</span></span>
  
> <span data-ttu-id="bd14e-116">[in]Unicode 文字列の先頭、末尾の null 文字を除いた文字数。</span><span class="sxs-lookup"><span data-stu-id="bd14e-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="bd14e-117">アプリケーションは、文字列が null で終わる場合、負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="bd14e-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="bd14e-118">この例では、 **MNLS_CompareStringW**関数は、長さを自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="bd14e-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="bd14e-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="bd14e-119">_pstr2_</span></span>
  
> <span data-ttu-id="bd14e-120">[in]比較する 2 番目の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bd14e-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="bd14e-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="bd14e-121">_cch2_</span></span>
  
> <span data-ttu-id="bd14e-122">[in]2 番目の Unicode 文字列は、終端の null 文字を除いた文字数。</span><span class="sxs-lookup"><span data-stu-id="bd14e-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="bd14e-123">アプリケーションは、文字列が null で終わる場合、負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="bd14e-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="bd14e-124">この場合、関数は長さを自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="bd14e-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bd14e-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="bd14e-125">Return value</span></span>

<span data-ttu-id="bd14e-126">[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)に記載されている値を返します。</span><span class="sxs-lookup"><span data-stu-id="bd14e-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd14e-127">備考</span><span class="sxs-lookup"><span data-stu-id="bd14e-127">Remarks</span></span>

<span data-ttu-id="bd14e-128">この関数は、 [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)をラップします。</span><span class="sxs-lookup"><span data-stu-id="bd14e-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="bd14e-129">**MNLS_CompareStringW**では、同じパラメーターを取得し、 [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)と同じ動作をしました。</span><span class="sxs-lookup"><span data-stu-id="bd14e-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bd14e-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd14e-130">See also</span></span>



[<span data-ttu-id="bd14e-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="bd14e-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="bd14e-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="bd14e-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

