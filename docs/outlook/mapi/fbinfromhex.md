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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414936"
---
# <a name="fbinfromhex"></a><span data-ttu-id="3c533-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="3c533-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="3c533-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c533-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c533-105">16進数値の文字列表現をバイナリデータに変換します。</span><span class="sxs-lookup"><span data-stu-id="3c533-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c533-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3c533-106">Header file:</span></span>  <br/> |<span data-ttu-id="3c533-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="3c533-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3c533-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="3c533-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3c533-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3c533-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3c533-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3c533-110">Called by:</span></span>  <br/> |<span data-ttu-id="3c533-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="3c533-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="3c533-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3c533-112">Parameters</span></span>

 <span data-ttu-id="3c533-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="3c533-113">_sz_</span></span>
  
> <span data-ttu-id="3c533-114">順番変換する null で終わる ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3c533-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="3c533-115">Unicode 文字列ではありません。</span><span class="sxs-lookup"><span data-stu-id="3c533-115">It is not a Unicode string.</span></span> <span data-ttu-id="3c533-116">有効な文字には、16進数の0から9までの文字、および大文字と小文字の両方が使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c533-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="3c533-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="3c533-117">_pb_</span></span>
  
> <span data-ttu-id="3c533-118">読み上げ返されたバイナリ番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3c533-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3c533-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="3c533-119">Return value</span></span>

<span data-ttu-id="3c533-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="3c533-120">TRUE</span></span> 
  
> <span data-ttu-id="3c533-121">文字列は、バイナリの数値に正しく変換されました。</span><span class="sxs-lookup"><span data-stu-id="3c533-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="3c533-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="3c533-122">FALSE</span></span> 
  
> <span data-ttu-id="3c533-123">入力文字列に無効な ASCII 16 進文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c533-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c533-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c533-124">See also</span></span>



[<span data-ttu-id="3c533-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="3c533-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

