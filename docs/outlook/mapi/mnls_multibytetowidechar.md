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
ms.openlocfilehash: 66e8c3b61caac6fb8d8b57d74ade6fa8aac3a9dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571707"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="c5bc4-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="c5bc4-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="c5bc4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5bc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5bc4-105">**MultiByteToWideChar**文字の文字列を utf-16 (ワイド文字) の文字列にマップするに似ています。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="c5bc4-106">文字の文字列とは限りませんマルチバイトの文字からは設定されません。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="c5bc4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c5bc4-107">Parameters</span></span>

 <span data-ttu-id="c5bc4-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="c5bc4-108">_uCodePage_</span></span>
  
> <span data-ttu-id="c5bc4-109">[in]変換の実行に使用するコード ページです。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="c5bc4-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="c5bc4-110">_dwFlags_</span></span>
  
> <span data-ttu-id="c5bc4-111">[in]変換の種類を示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="c5bc4-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="c5bc4-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="c5bc4-113">[in]変換する文字の文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="c5bc4-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="c5bc4-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="c5bc4-115">[in]_LpMultiByteStr_パラメーターで指定された文字列のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="c5bc4-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="c5bc4-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="c5bc4-117">[out]省略可能です。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-117">[out] Optional.</span></span> <span data-ttu-id="c5bc4-118">変換後の文字列を受け取るバッファーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="c5bc4-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="c5bc4-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="c5bc4-120">[in]_LpWideCharStr_で示されるバッファーの文字のサイズです。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5bc4-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="c5bc4-121">Return value</span></span>

<span data-ttu-id="c5bc4-122">正常終了した場合は、 _lpWideCharStr_で示されるバッファーに書き込まれた文字数を返します。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c5bc4-123">注釈</span><span class="sxs-lookup"><span data-stu-id="c5bc4-123">Remarks</span></span>

<span data-ttu-id="c5bc4-124">この関数は、 **MultiByteToWideChar**の関数をラップします。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="c5bc4-125">詳細については、 [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5bc4-125">For more information, see [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span></span>
  

