---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338732"
---
# <a name="mnls_widechartomultibyte"></a><span data-ttu-id="7c894-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="7c894-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="7c894-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c894-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c894-105">この関数は、UTF-16 (ワイド文字) 文字列を新しい文字列にマップする **WideCharToMultiByte** に似ています。</span><span class="sxs-lookup"><span data-stu-id="7c894-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="7c894-106">新しい文字列は、必ずしもマルチバイト文字セットとは限りません。</span><span class="sxs-lookup"><span data-stu-id="7c894-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7c894-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7c894-107">Parameters</span></span>

 <span data-ttu-id="7c894-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="7c894-108">_uCodePage_</span></span>
  
> <span data-ttu-id="7c894-109">[in]変換の実行に使用するコード ページ。</span><span class="sxs-lookup"><span data-stu-id="7c894-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="7c894-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="7c894-110">_dwFlags_</span></span>
  
> <span data-ttu-id="7c894-111">[in]変換の種類を示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="7c894-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="7c894-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="7c894-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="7c894-113">[in]変換する Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7c894-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="7c894-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="7c894-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="7c894-115">[in]変換の種類を示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="7c894-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="7c894-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="7c894-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="7c894-117">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="7c894-117">[out] Optional.</span></span> <span data-ttu-id="7c894-118">変換された文字列を受け取るバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7c894-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="7c894-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="7c894-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="7c894-120">[in]  _lpMultiByteStr_ で示されるバッファーのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="7c894-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="7c894-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="7c894-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="7c894-122">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="7c894-122">[in] Optional.</span></span> <span data-ttu-id="7c894-123">指定したコード ページで文字を表現できない場合に使用する文字へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7c894-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="7c894-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="7c894-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="7c894-125">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="7c894-125">[out] Optional.</span></span> <span data-ttu-id="7c894-126">関数が変換で既定の文字を使用したかどうかを示すフラグへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7c894-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c894-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="7c894-127">Return value</span></span>

<span data-ttu-id="7c894-128">成功した場合  _、lpMultiByteStr_ が指すバッファーに書き込まれたバイト数を返します。</span><span class="sxs-lookup"><span data-stu-id="7c894-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7c894-129">注釈</span><span class="sxs-lookup"><span data-stu-id="7c894-129">Remarks</span></span>

<span data-ttu-id="7c894-130">この関数は **、WideCharToMultiByte 関数をラップ** します。</span><span class="sxs-lookup"><span data-stu-id="7c894-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="7c894-131">詳細については [、「WideCharToMultiByte」を参照してください](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7c894-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c894-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c894-132">See also</span></span>



[<span data-ttu-id="7c894-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="7c894-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

