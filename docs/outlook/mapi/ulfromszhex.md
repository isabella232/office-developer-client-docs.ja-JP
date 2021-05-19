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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433053"
---
# <a name="ulfromszhex"></a><span data-ttu-id="b69c8-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="b69c8-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="b69c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b69c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b69c8-105">16 進数の null 終端文字列を符号なし長整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="b69c8-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b69c8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b69c8-106">Header file:</span></span>  <br/> |<span data-ttu-id="b69c8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b69c8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b69c8-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="b69c8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b69c8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b69c8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b69c8-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b69c8-110">Called by:</span></span>  <br/> |<span data-ttu-id="b69c8-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b69c8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="b69c8-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b69c8-112">Parameters</span></span>

 <span data-ttu-id="b69c8-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="b69c8-113">_lpsz_</span></span>
  
> <span data-ttu-id="b69c8-114">[in]変換する null 終端文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b69c8-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="b69c8-115">_lpsz パラメーター_ は、65536 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="b69c8-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b69c8-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="b69c8-116">Return value</span></span>

 <span data-ttu-id="b69c8-117">**UlFromSzHex は** 、符号なし長整数を返します。</span><span class="sxs-lookup"><span data-stu-id="b69c8-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="b69c8-118">文字列が 1 桁以上の 16 進数で始まる場合は、ゼロが返されます。</span><span class="sxs-lookup"><span data-stu-id="b69c8-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b69c8-119">注釈</span><span class="sxs-lookup"><span data-stu-id="b69c8-119">Remarks</span></span>

<span data-ttu-id="b69c8-120">**UlFromSzHex** 関数は、16 進数ではない文字列の最初の文字に達すると、変換を停止します。</span><span class="sxs-lookup"><span data-stu-id="b69c8-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="b69c8-121">たとえば、文字列 "5a" を指定すると **、UlFromSzHex** は整数値 90 を返します。</span><span class="sxs-lookup"><span data-stu-id="b69c8-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="b69c8-122">文字列 "5g5h" を指定すると、整数値 5 が返されます。</span><span class="sxs-lookup"><span data-stu-id="b69c8-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="b69c8-123">文字列 "g5h5" を指定すると **、UlFromSzHex は** ゼロを返します。</span><span class="sxs-lookup"><span data-stu-id="b69c8-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="b69c8-124">**UlFromSzHex** は、二次的な違いには敏感ですが、16 進数の場合は 'a' から 'f' と 'A' から 'F' の両方を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b69c8-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="b69c8-125">Unicode および DBCS 形式の文字列がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b69c8-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="b69c8-126">_lpsz の長さの制限は_ 文字で、必ずしもバイトではありません。</span><span class="sxs-lookup"><span data-stu-id="b69c8-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

