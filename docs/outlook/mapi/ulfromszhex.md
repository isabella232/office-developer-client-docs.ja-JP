---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315366"
---
# <a name="ulfromszhex"></a><span data-ttu-id="a437c-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="a437c-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="a437c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a437c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a437c-105">null で終わる16進数値の文字列を、符号なしの長整数型 (long) の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="a437c-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a437c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a437c-106">Header file:</span></span>  <br/> |<span data-ttu-id="a437c-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a437c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a437c-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="a437c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a437c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a437c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a437c-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a437c-110">Called by:</span></span>  <br/> |<span data-ttu-id="a437c-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="a437c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="a437c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a437c-112">Parameters</span></span>

 <span data-ttu-id="a437c-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a437c-113">_lpsz_</span></span>
  
> <span data-ttu-id="a437c-114">順番変換する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a437c-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="a437c-115">_lpsz_パラメーターは、65536文字以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a437c-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a437c-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="a437c-116">Return value</span></span>

 <span data-ttu-id="a437c-117">**ulfromszhex**は、符号なし長整数型 (long) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="a437c-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="a437c-118">文字列の先頭に少なくとも1つの16進数が指定されていない場合は、0が返されます。</span><span class="sxs-lookup"><span data-stu-id="a437c-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a437c-119">解説</span><span class="sxs-lookup"><span data-stu-id="a437c-119">Remarks</span></span>

<span data-ttu-id="a437c-120">**ulfromszhex**関数は、16進数ではない文字列の最初の文字に達したときに変換を停止します。</span><span class="sxs-lookup"><span data-stu-id="a437c-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="a437c-121">たとえば、文字列 "5a" が指定されている場合、 **ulfromszhex**は整数値90を返します。</span><span class="sxs-lookup"><span data-stu-id="a437c-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="a437c-122">文字列 "5g5h" が指定されている場合、この関数は整数値5を返します。</span><span class="sxs-lookup"><span data-stu-id="a437c-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="a437c-123">文字列 "g5h5" が指定されている場合、 **ulfromszhex**は0を返します。</span><span class="sxs-lookup"><span data-stu-id="a437c-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="a437c-124">**ulfromszhex**は、発音区別の違いに注意していますが、' a ' ~ ' f ' の両方と ' a ' ~ ' a ' を16進数の数字に対して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a437c-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="a437c-125">Unicode および DBCS 形式の文字列がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a437c-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="a437c-126">_lpsz_の長さの制限は、文字である必要があり、必ずしもバイトではありません。</span><span class="sxs-lookup"><span data-stu-id="a437c-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

