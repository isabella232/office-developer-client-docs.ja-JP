---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338242"
---
# <a name="mnls_multibytetowidechar"></a><span data-ttu-id="4ffe7-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="4ffe7-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="4ffe7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ffe7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ffe7-105">**MultiByteToWideChar** と同様に、文字列を UTF-16 (ワイド文字) 文字列にマップします。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="4ffe7-106">文字列は、必ずしもマルチバイト文字セットとは限りません。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="4ffe7-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4ffe7-107">Parameters</span></span>

 <span data-ttu-id="4ffe7-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="4ffe7-108">_uCodePage_</span></span>
  
> <span data-ttu-id="4ffe7-109">[in]変換の実行に使用するコード ページ。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="4ffe7-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4ffe7-110">_dwFlags_</span></span>
  
> <span data-ttu-id="4ffe7-111">[in]変換の種類を示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="4ffe7-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="4ffe7-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="4ffe7-113">[in]変換する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="4ffe7-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="4ffe7-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="4ffe7-115">[in]  _lpMultiByteStr_ パラメーターで示される文字列のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="4ffe7-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="4ffe7-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="4ffe7-117">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-117">[out] Optional.</span></span> <span data-ttu-id="4ffe7-118">変換された文字列を受け取るバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="4ffe7-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="4ffe7-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="4ffe7-120">[in]  _lpWideCharStr_ で示されるバッファーのサイズ (文字)。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ffe7-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="4ffe7-121">Return value</span></span>

<span data-ttu-id="4ffe7-122">成功した場合  _、lpWideCharStr_ で示されるバッファーに書き込まれた文字数を返します。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4ffe7-123">注釈</span><span class="sxs-lookup"><span data-stu-id="4ffe7-123">Remarks</span></span>

<span data-ttu-id="4ffe7-124">この関数は **、MultiByteToWideChar 関数をラップ** します。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="4ffe7-125">詳細については [、「MultiByteToWideChar」を参照してください](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4ffe7-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

