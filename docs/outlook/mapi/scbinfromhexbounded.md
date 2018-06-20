---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803807"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="756ba-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="756ba-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="756ba-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="756ba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="756ba-105">16 進数の文字列形式の指定部分を 2 進数に変換します。</span><span class="sxs-lookup"><span data-stu-id="756ba-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="756ba-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="756ba-106">Header file:</span></span>  <br/> |<span data-ttu-id="756ba-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="756ba-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="756ba-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="756ba-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="756ba-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="756ba-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="756ba-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="756ba-110">Called by:</span></span>  <br/> |<span data-ttu-id="756ba-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="756ba-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="756ba-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="756ba-112">Parameters</span></span>

 <span data-ttu-id="756ba-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="756ba-113">_sz_</span></span>
  
> <span data-ttu-id="756ba-114">[in]変換される null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="756ba-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="756ba-115">有効な文字には、9 との両方の大文字と小文字の文字を 16 進数の文字 0 ~ f が含まれます。</span><span class="sxs-lookup"><span data-stu-id="756ba-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="756ba-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="756ba-116">_pb_</span></span>
  
> <span data-ttu-id="756ba-117">[out]返される 2 進数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="756ba-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="756ba-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="756ba-118">_cb_</span></span>
  
> <span data-ttu-id="756ba-119">[in]_Pb_パラメーターのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="756ba-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="756ba-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="756ba-120">Return value</span></span>

<span data-ttu-id="756ba-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="756ba-121">S_OK</span></span>
  
> <span data-ttu-id="756ba-122">変換に成功しました。</span><span class="sxs-lookup"><span data-stu-id="756ba-122">Conversion was successful.</span></span>
    
<span data-ttu-id="756ba-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="756ba-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="756ba-124">無効な文字が発生しました。</span><span class="sxs-lookup"><span data-stu-id="756ba-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="756ba-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="756ba-125">See also</span></span>



[<span data-ttu-id="756ba-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="756ba-126">FBinFromHex</span></span>](fbinfromhex.md)

