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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356848"
---
# <a name="mnls_comparestringw"></a><span data-ttu-id="a42a4-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="a42a4-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="a42a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a42a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a42a4-105">2 つの Unicode 文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="a42a4-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="a42a4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a42a4-106">Parameters</span></span>

 <span data-ttu-id="a42a4-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="a42a4-107">_lcid_</span></span>
  
> <span data-ttu-id="a42a4-108">[in]ロケール識別子。</span><span class="sxs-lookup"><span data-stu-id="a42a4-108">[in] Locale identifier.</span></span> <span data-ttu-id="a42a4-109">詳細な定義については  _、CompareString の Locale_ パラメーターを [参照してください](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a42a4-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="a42a4-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="a42a4-110">_dwFlags_</span></span>
  
> <span data-ttu-id="a42a4-111">[in]大文字と小文字の区別を無視するフラグ。</span><span class="sxs-lookup"><span data-stu-id="a42a4-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="a42a4-112">詳細な定義については  _、CompareStringEx の dwCmpFlags_ パラメーター [を参照してください](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a42a4-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="a42a4-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="a42a4-113">_pstr1_</span></span>
  
> <span data-ttu-id="a42a4-114">[in]比較する最初の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a42a4-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="a42a4-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="a42a4-115">_cch1_</span></span>
  
> <span data-ttu-id="a42a4-116">[in]終端の null 文字を除く、最初の Unicode 文字列の文字の長さ。</span><span class="sxs-lookup"><span data-stu-id="a42a4-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="a42a4-117">文字列が null 終端の場合、アプリケーションは負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a42a4-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="a42a4-118">この場合、この関数 **はMNLS_CompareStringW** 長さを自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="a42a4-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="a42a4-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="a42a4-119">_pstr2_</span></span>
  
> <span data-ttu-id="a42a4-120">[in]比較する 2 番目の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a42a4-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="a42a4-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="a42a4-121">_cch2_</span></span>
  
> <span data-ttu-id="a42a4-122">[in]2 番目の Unicode 文字列の文字の長さ (終端の null 文字を除く)。</span><span class="sxs-lookup"><span data-stu-id="a42a4-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="a42a4-123">文字列が null 終端の場合、アプリケーションは負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a42a4-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="a42a4-124">この場合、関数は自動的に長さを決定します。</span><span class="sxs-lookup"><span data-stu-id="a42a4-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a42a4-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="a42a4-125">Return value</span></span>

<span data-ttu-id="a42a4-126">CompareStringEx で説明されている [値を返します](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a42a4-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a42a4-127">注釈</span><span class="sxs-lookup"><span data-stu-id="a42a4-127">Remarks</span></span>

<span data-ttu-id="a42a4-128">この関数は [CompareStringW をラップします](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a42a4-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="a42a4-129">**MNLS_CompareStringW** 同じパラメーターを受け取り [、CompareStringW と同じ動作をします](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a42a4-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a42a4-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="a42a4-130">See also</span></span>



[<span data-ttu-id="a42a4-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="a42a4-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="a42a4-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="a42a4-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

