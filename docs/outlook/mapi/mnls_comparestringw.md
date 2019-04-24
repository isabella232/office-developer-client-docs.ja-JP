---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: '最終更新日: 2012 年2月20日'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356848"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="43bbf-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="43bbf-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="43bbf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43bbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43bbf-105">2つの Unicode 文字列を比較します。</span><span class="sxs-lookup"><span data-stu-id="43bbf-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="43bbf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="43bbf-106">Parameters</span></span>

 <span data-ttu-id="43bbf-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="43bbf-107">_lcid_</span></span>
  
> <span data-ttu-id="43bbf-108">順番ロケール識別子。</span><span class="sxs-lookup"><span data-stu-id="43bbf-108">[in] Locale identifier.</span></span> <span data-ttu-id="43bbf-109">詳細な定義については、 [comparestring](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)の_Locale_パラメーターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="43bbf-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="43bbf-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="43bbf-110">_dwFlags_</span></span>
  
> <span data-ttu-id="43bbf-111">順番大文字/小文字の区別を無視するフラグ。</span><span class="sxs-lookup"><span data-stu-id="43bbf-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="43bbf-112">詳細な定義については、 _dwCmpFlags_パラメータ of [comparestringex](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43bbf-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="43bbf-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="43bbf-113">_pstr1_</span></span>
  
> <span data-ttu-id="43bbf-114">順番比較する最初の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="43bbf-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="43bbf-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="43bbf-115">_cch1_</span></span>
  
> <span data-ttu-id="43bbf-116">順番最初の Unicode 文字列の文字数 (終端の null 文字は除く)。</span><span class="sxs-lookup"><span data-stu-id="43bbf-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="43bbf-117">文字列が null で終端されている場合、アプリケーションは負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="43bbf-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="43bbf-118">この場合、 **MNLS_CompareStringW**関数は長さを自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="43bbf-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="43bbf-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="43bbf-119">_pstr2_</span></span>
  
> <span data-ttu-id="43bbf-120">順番比較する2番目の Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="43bbf-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="43bbf-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="43bbf-121">_cch2_</span></span>
  
> <span data-ttu-id="43bbf-122">順番2番目の Unicode 文字列の文字数 (終端の null 文字は除く)。</span><span class="sxs-lookup"><span data-stu-id="43bbf-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="43bbf-123">文字列が null で終端されている場合、アプリケーションは負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="43bbf-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="43bbf-124">この場合、関数は長さを自動的に決定します。</span><span class="sxs-lookup"><span data-stu-id="43bbf-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="43bbf-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="43bbf-125">Return value</span></span>

<span data-ttu-id="43bbf-126">[comparestringex](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)で記述されている値を返します。</span><span class="sxs-lookup"><span data-stu-id="43bbf-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43bbf-127">解説</span><span class="sxs-lookup"><span data-stu-id="43bbf-127">Remarks</span></span>

<span data-ttu-id="43bbf-128">この関数は、 [comparestringw](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)をラップします。</span><span class="sxs-lookup"><span data-stu-id="43bbf-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="43bbf-129">**MNLS_CompareStringW**は同じパラメーターを受け取り、 [comparestringw](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)と同じ動作をします。</span><span class="sxs-lookup"><span data-stu-id="43bbf-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43bbf-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="43bbf-130">See also</span></span>



[<span data-ttu-id="43bbf-131">comparestringw</span><span class="sxs-lookup"><span data-stu-id="43bbf-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="43bbf-132">comparestringex</span><span class="sxs-lookup"><span data-stu-id="43bbf-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

