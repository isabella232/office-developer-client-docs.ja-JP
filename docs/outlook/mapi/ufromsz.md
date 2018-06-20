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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5be5cd7c352201159c0257861c0072b56da65082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804173"
---
# <a name="ufromsz"></a><span data-ttu-id="0c375-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="0c375-103">UFromSz</span></span>

  
  
<span data-ttu-id="0c375-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c375-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c375-105">以下の桁数、null で終わる文字列を符号なし整数に変換します。</span><span class="sxs-lookup"><span data-stu-id="0c375-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c375-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0c375-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c375-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c375-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0c375-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0c375-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c375-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0c375-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0c375-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0c375-110">Called by:</span></span>  <br/> |<span data-ttu-id="0c375-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0c375-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="0c375-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0c375-112">Parameters</span></span>

 <span data-ttu-id="0c375-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="0c375-113">_lpsz_</span></span>
  
> <span data-ttu-id="0c375-114">[in]変換される null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c375-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="0c375-115">_Lpsz_パラメーターは、65536 文字を超えない必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c375-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0c375-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0c375-116">Return value</span></span>

 <span data-ttu-id="0c375-117">**UFromSz**では、符号なし整数を返します。</span><span class="sxs-lookup"><span data-stu-id="0c375-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="0c375-118">文字列は、少なくとも 1 つの 10 進数字で始まらない、ゼロが返されます。</span><span class="sxs-lookup"><span data-stu-id="0c375-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0c375-119">備考</span><span class="sxs-lookup"><span data-stu-id="0c375-119">Remarks</span></span>

<span data-ttu-id="0c375-120">**UFromSz**関数では、10 進の数字ではない文字列の最初の文字に達したときの変換を停止します。</span><span class="sxs-lookup"><span data-stu-id="0c375-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="0c375-121">**UFromSz**は、「55」という文字列を指定するには、55 の整数値を返します。</span><span class="sxs-lookup"><span data-stu-id="0c375-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="0c375-122">文字列"5a5b"を指定するには、この関数は、整数値 5 を返します。</span><span class="sxs-lookup"><span data-stu-id="0c375-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="0c375-123">"A5b5"という文字列を指定するには、 **UFromSz**は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="0c375-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="0c375-124">**UFromSz**は、アクセントの違いに敏感です。</span><span class="sxs-lookup"><span data-stu-id="0c375-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="0c375-125">Unicode と DBCS の形式で文字列がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0c375-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="0c375-126">_Lpsz_の長さの制限は、文字数、バイト数ではありませんが。</span><span class="sxs-lookup"><span data-stu-id="0c375-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

