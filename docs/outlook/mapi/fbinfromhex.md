---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800057"
---
# <a name="fbinfromhex"></a><span data-ttu-id="2769f-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="2769f-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="2769f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2769f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2769f-105">バイナリ データを 16 進数の文字列形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="2769f-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2769f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2769f-106">Header file:</span></span>  <br/> |<span data-ttu-id="2769f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2769f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2769f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2769f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2769f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2769f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2769f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2769f-110">Called by:</span></span>  <br/> |<span data-ttu-id="2769f-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2769f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="2769f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2769f-112">Parameters</span></span>

 <span data-ttu-id="2769f-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="2769f-113">_sz_</span></span>
  
> <span data-ttu-id="2769f-114">[in]変換する null で終わる ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2769f-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="2769f-115">Unicode 文字列ではありません。</span><span class="sxs-lookup"><span data-stu-id="2769f-115">It is not a Unicode string.</span></span> <span data-ttu-id="2769f-116">有効な文字には、9 つと両方大文字と小文字の文字 A f を 16 進文字 0 にはが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2769f-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="2769f-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="2769f-117">_pb_</span></span>
  
> <span data-ttu-id="2769f-118">[out]返される 2 進数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2769f-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2769f-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="2769f-119">Return value</span></span>

<span data-ttu-id="2769f-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="2769f-120">TRUE</span></span> 
  
> <span data-ttu-id="2769f-121">文字列は、2 進数に正常に変換されました。</span><span class="sxs-lookup"><span data-stu-id="2769f-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="2769f-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="2769f-122">FALSE</span></span> 
  
> <span data-ttu-id="2769f-123">入力文字列には、無効な ASCII 16 進数文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2769f-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2769f-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="2769f-124">See also</span></span>



[<span data-ttu-id="2769f-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="2769f-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

