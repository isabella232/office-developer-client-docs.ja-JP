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
ms.openlocfilehash: 6957888f6727175d73d277cf4f5b84dc234d22ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570038"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="9b4f2-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="9b4f2-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="9b4f2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b4f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b4f2-105">この関数は、 **WideCharToMultiByte**utf-16 (ワイド文字) の文字列を新しい文字列にマップするに似ています。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="9b4f2-106">新しい文字の文字列とは限りませんマルチバイトの文字からは設定されません。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="9b4f2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9b4f2-107">Parameters</span></span>

 <span data-ttu-id="9b4f2-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="9b4f2-108">_uCodePage_</span></span>
  
> <span data-ttu-id="9b4f2-109">[in]変換の実行に使用するコード ページです。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="9b4f2-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="9b4f2-110">_dwFlags_</span></span>
  
> <span data-ttu-id="9b4f2-111">[in]変換の種類を示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="9b4f2-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="9b4f2-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="9b4f2-113">[in]変換する Unicode 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="9b4f2-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="9b4f2-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="9b4f2-115">[in]変換の種類を示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="9b4f2-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="9b4f2-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="9b4f2-117">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-117">[out] Optional.</span></span> <span data-ttu-id="9b4f2-118">変換後の文字列を受け取るバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="9b4f2-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="9b4f2-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="9b4f2-120">[in]_LpMultiByteStr_で示されるバッファーのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="9b4f2-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="9b4f2-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="9b4f2-122">[in]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-122">[in] Optional.</span></span> <span data-ttu-id="9b4f2-123">指定したコード ページで文字を表現できない場合に使用する文字へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="9b4f2-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="9b4f2-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="9b4f2-125">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-125">[out] Optional.</span></span> <span data-ttu-id="9b4f2-126">関数が変換時に既定の文字を使用されるかどうかであることを示すフラグへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b4f2-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="9b4f2-127">Return value</span></span>

<span data-ttu-id="9b4f2-128">正常終了した場合、 _lpMultiByteStr_が指すバッファーに書き込まれたバイト数を返します。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9b4f2-129">注釈</span><span class="sxs-lookup"><span data-stu-id="9b4f2-129">Remarks</span></span>

<span data-ttu-id="9b4f2-130">この関数は、 **WideCharToMultiByte**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="9b4f2-131">詳細については、 [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b4f2-131">For more information, see [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b4f2-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b4f2-132">See also</span></span>



[<span data-ttu-id="9b4f2-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="9b4f2-133">WideCharToMultiByte</span></span>](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

