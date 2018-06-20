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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d5ba7e7bc52ba041e9fe6c9a01b35dc91d3b947b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804163"
---
# <a name="ulfromszhex"></a><span data-ttu-id="e4966-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="e4966-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="e4966-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4966-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4966-105">16 進数の null で終わる文字列を符号なし長整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="e4966-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4966-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e4966-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4966-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4966-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e4966-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e4966-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e4966-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e4966-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e4966-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e4966-110">Called by:</span></span>  <br/> |<span data-ttu-id="e4966-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e4966-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="e4966-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4966-112">Parameters</span></span>

 <span data-ttu-id="e4966-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e4966-113">_lpsz_</span></span>
  
> <span data-ttu-id="e4966-114">[in]変換される null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e4966-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="e4966-115">_Lpsz_パラメーターは、65536 文字を超えない必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4966-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e4966-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e4966-116">Return value</span></span>

 <span data-ttu-id="e4966-117">**UlFromSzHex**では、符号なし長整数を返します。</span><span class="sxs-lookup"><span data-stu-id="e4966-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="e4966-118">文字列は、16 進数を少なくとも 1 つで開始されていない、0 が返されます。</span><span class="sxs-lookup"><span data-stu-id="e4966-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e4966-119">備考</span><span class="sxs-lookup"><span data-stu-id="e4966-119">Remarks</span></span>

<span data-ttu-id="e4966-120">**UlFromSzHex**関数は、16 進数ではない文字列の最初の文字に達したときの変換を停止します。</span><span class="sxs-lookup"><span data-stu-id="e4966-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="e4966-121">**UlFromSzHex**は、"5 a"の文字列を指定するには、90 の整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="e4966-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="e4966-122">文字列"5g5h"を指定するには、この関数は、整数値 5 を返します。</span><span class="sxs-lookup"><span data-stu-id="e4966-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="e4966-123">文字列"g5h5"を指定するには、 **UlFromSzHex**は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="e4966-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="e4966-124">**UlFromSzHex**アクセントの違いに左右されるがの ' a' から 'f' と '、' 'F' までの 16 進数にします。</span><span class="sxs-lookup"><span data-stu-id="e4966-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="e4966-125">Unicode と DBCS の形式で文字列がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e4966-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="e4966-126">_Lpsz_の長さの制限は、文字数、バイト数ではありませんが。</span><span class="sxs-lookup"><span data-stu-id="e4966-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

