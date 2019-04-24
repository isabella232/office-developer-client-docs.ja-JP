---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: '最終更新日: 2012 年2月21日'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338732"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="53de3-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="53de3-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="53de3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53de3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53de3-105">この関数は**WideCharToMultiByte**に似ています。これは、utf-16 (ワイド文字) 文字列を新しい文字列にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="53de3-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="53de3-106">新しい文字列は、マルチバイト文字セットからのものであるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="53de3-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a><span data-ttu-id="53de3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="53de3-107">Parameters</span></span>

 <span data-ttu-id="53de3-108">_ucodepage_</span><span class="sxs-lookup"><span data-stu-id="53de3-108">_uCodePage_</span></span>
  
> <span data-ttu-id="53de3-109">順番変換を実行するために使用するコードページ。</span><span class="sxs-lookup"><span data-stu-id="53de3-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="53de3-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="53de3-110">_dwFlags_</span></span>
  
> <span data-ttu-id="53de3-111">順番変換の種類を示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="53de3-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="53de3-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="53de3-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="53de3-113">順番変換する Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="53de3-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="53de3-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="53de3-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="53de3-115">順番変換の種類を示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="53de3-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="53de3-116">_lpmultibytestr_</span><span class="sxs-lookup"><span data-stu-id="53de3-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="53de3-117">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="53de3-117">[out] Optional.</span></span> <span data-ttu-id="53de3-118">変換された文字列を受け取るバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="53de3-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="53de3-119">_cchmultibyte バイト_</span><span class="sxs-lookup"><span data-stu-id="53de3-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="53de3-120">順番_lpmultibytestr_によって示されるバッファーのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="53de3-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="53de3-121">_lpdefaultchar_</span><span class="sxs-lookup"><span data-stu-id="53de3-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="53de3-122">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="53de3-122">[in] Optional.</span></span> <span data-ttu-id="53de3-123">指定されたコードページで文字を表現できない場合に使用する文字へのポインター。</span><span class="sxs-lookup"><span data-stu-id="53de3-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="53de3-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="53de3-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="53de3-125">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="53de3-125">[out] Optional.</span></span> <span data-ttu-id="53de3-126">関数が変換時に既定の文字を使用したかどうかを示すフラグへのポインター。</span><span class="sxs-lookup"><span data-stu-id="53de3-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53de3-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="53de3-127">Return value</span></span>

<span data-ttu-id="53de3-128">成功した場合は、 _lpmultibytestr_が指すバッファーに書き込まれたバイト数を返します。</span><span class="sxs-lookup"><span data-stu-id="53de3-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="53de3-129">解説</span><span class="sxs-lookup"><span data-stu-id="53de3-129">Remarks</span></span>

<span data-ttu-id="53de3-130">この関数は、 **WideCharToMultiByte**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="53de3-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="53de3-131">詳細については、「 [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53de3-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53de3-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="53de3-132">See also</span></span>



[<span data-ttu-id="53de3-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="53de3-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

