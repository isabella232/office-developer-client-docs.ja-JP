---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: '最終更新日: 2012 年2月21日'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338242"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="07815-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="07815-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="07815-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07815-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07815-105">**MultiByteToWideChar**に似ています。これは、文字列を utf-16 (ワイド文字) 文字列にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="07815-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="07815-106">文字文字列は、マルチバイト文字セットからのものであるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="07815-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="07815-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07815-107">Parameters</span></span>

 <span data-ttu-id="07815-108">_ucodepage_</span><span class="sxs-lookup"><span data-stu-id="07815-108">_uCodePage_</span></span>
  
> <span data-ttu-id="07815-109">順番変換を実行するために使用するコードページ。</span><span class="sxs-lookup"><span data-stu-id="07815-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="07815-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="07815-110">_dwFlags_</span></span>
  
> <span data-ttu-id="07815-111">順番変換の種類を示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="07815-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="07815-112">_lpmultibytestr_</span><span class="sxs-lookup"><span data-stu-id="07815-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="07815-113">順番変換する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="07815-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="07815-114">_cchmultibyte バイト_</span><span class="sxs-lookup"><span data-stu-id="07815-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="07815-115">順番_lpmultibytestr_パラメーターで指定された文字列のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="07815-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="07815-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="07815-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="07815-117">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="07815-117">[out] Optional.</span></span> <span data-ttu-id="07815-118">変換された文字列を受け取るバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="07815-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="07815-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="07815-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="07815-120">順番_lpWideCharStr_によって示されるバッファーのサイズ (文字数)。</span><span class="sxs-lookup"><span data-stu-id="07815-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07815-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="07815-121">Return value</span></span>

<span data-ttu-id="07815-122">成功した場合、 _lpWideCharStr_によって示されるバッファーに書き込まれた文字数を返します。</span><span class="sxs-lookup"><span data-stu-id="07815-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07815-123">解説</span><span class="sxs-lookup"><span data-stu-id="07815-123">Remarks</span></span>

<span data-ttu-id="07815-124">この関数は、 **MultiByteToWideChar**関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="07815-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="07815-125">詳細については、「 [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07815-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

