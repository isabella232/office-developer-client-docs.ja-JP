---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439010"
---
# <a name="ufromsz"></a><span data-ttu-id="b86bf-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="b86bf-103">UFromSz</span></span>

  
  
<span data-ttu-id="b86bf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b86bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b86bf-105">10進数値の null で終わる文字列を符号なし整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="b86bf-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b86bf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b86bf-106">Header file:</span></span>  <br/> |<span data-ttu-id="b86bf-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b86bf-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b86bf-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="b86bf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b86bf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b86bf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b86bf-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b86bf-110">Called by:</span></span>  <br/> |<span data-ttu-id="b86bf-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="b86bf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="b86bf-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b86bf-112">Parameters</span></span>

 <span data-ttu-id="b86bf-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="b86bf-113">_lpsz_</span></span>
  
> <span data-ttu-id="b86bf-114">順番変換する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b86bf-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="b86bf-115">_lpsz_パラメーターは、65536文字以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b86bf-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b86bf-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="b86bf-116">Return value</span></span>

 <span data-ttu-id="b86bf-117">**ufromsz**は、符号なし整数を返します。</span><span class="sxs-lookup"><span data-stu-id="b86bf-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="b86bf-118">文字列が少なくとも1つの10進数字で始まらない場合は、0が返されます。</span><span class="sxs-lookup"><span data-stu-id="b86bf-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b86bf-119">注釈</span><span class="sxs-lookup"><span data-stu-id="b86bf-119">Remarks</span></span>

<span data-ttu-id="b86bf-120">**ufromsz**関数は、10進数ではない文字列の最初の文字に達したときに変換を停止します。</span><span class="sxs-lookup"><span data-stu-id="b86bf-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="b86bf-121">たとえば、文字列 "55" が指定されている場合、 **ufromsz**は整数値55を返します。</span><span class="sxs-lookup"><span data-stu-id="b86bf-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="b86bf-122">文字列 "5a5b" が指定されている場合、関数は整数値5を返します。</span><span class="sxs-lookup"><span data-stu-id="b86bf-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="b86bf-123">文字列 "a5b5" が指定されている場合、 **ufromsz**は0を返します。</span><span class="sxs-lookup"><span data-stu-id="b86bf-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="b86bf-124">**ufromsz**は、分音の違いに敏感です。</span><span class="sxs-lookup"><span data-stu-id="b86bf-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="b86bf-125">Unicode および DBCS 形式の文字列がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b86bf-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="b86bf-126">_lpsz_の長さの制限は、文字である必要があり、必ずしもバイトではありません。</span><span class="sxs-lookup"><span data-stu-id="b86bf-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

