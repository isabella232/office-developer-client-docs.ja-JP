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
ms.openlocfilehash: f7889a255e2aa8ea4b6908f2f10a7b546a8ee3f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801642"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="aa85f-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="aa85f-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="aa85f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa85f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa85f-105">2 つの Unicode 文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="aa85f-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="aa85f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aa85f-106">Parameters</span></span>

 <span data-ttu-id="aa85f-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="aa85f-107">_lcid_</span></span>
  
> <span data-ttu-id="aa85f-108">[in]ロケール識別子です。</span><span class="sxs-lookup"><span data-stu-id="aa85f-108">[in] Locale identifier.</span></span> <span data-ttu-id="aa85f-109">詳細な定義は、[通常](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)の_ロケール_パラメーターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa85f-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="aa85f-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="aa85f-110">_dwFlags_</span></span>
  
> <span data-ttu-id="aa85f-111">[in]大文字と小文字およびアクセント記号を無視するようにフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="aa85f-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="aa85f-112">詳細な定義は、 [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)の_dwCmpFlags_パラメーターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa85f-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="aa85f-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="aa85f-113">_pstr1_</span></span>
  
> <span data-ttu-id="aa85f-114">[in]比較する最初の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa85f-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="aa85f-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="aa85f-115">_cch1_</span></span>
  
> <span data-ttu-id="aa85f-116">[in]Unicode 文字列の先頭、末尾の null 文字を除いた文字数。</span><span class="sxs-lookup"><span data-stu-id="aa85f-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="aa85f-117">アプリケーションは、文字列が null で終わる場合、負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="aa85f-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="aa85f-118">この例では、 **MNLS_CompareStringW**関数は、長さを自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="aa85f-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="aa85f-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="aa85f-119">_pstr2_</span></span>
  
> <span data-ttu-id="aa85f-120">[in]比較する 2 番目の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="aa85f-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="aa85f-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="aa85f-121">_cch2_</span></span>
  
> <span data-ttu-id="aa85f-122">[in]2 番目の Unicode 文字列は、終端の null 文字を除いた文字数。</span><span class="sxs-lookup"><span data-stu-id="aa85f-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="aa85f-123">アプリケーションは、文字列が null で終わる場合、負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="aa85f-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="aa85f-124">この場合、関数は長さを自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="aa85f-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa85f-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="aa85f-125">Return value</span></span>

<span data-ttu-id="aa85f-126">[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)に記載されている値を返します。</span><span class="sxs-lookup"><span data-stu-id="aa85f-126">Returns the values described for [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa85f-127">注釈</span><span class="sxs-lookup"><span data-stu-id="aa85f-127">Remarks</span></span>

<span data-ttu-id="aa85f-128">この関数は、 [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)をラップします。</span><span class="sxs-lookup"><span data-stu-id="aa85f-128">This function wraps [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="aa85f-129">**MNLS_CompareStringW**では、同じパラメーターを取得し、 [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)と同じ動作をしました。</span><span class="sxs-lookup"><span data-stu-id="aa85f-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa85f-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa85f-130">See also</span></span>



[<span data-ttu-id="aa85f-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="aa85f-131">CompareStringW</span></span>](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="aa85f-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="aa85f-132">CompareStringEx</span></span>](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

