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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439759"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="04b8f-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="04b8f-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="04b8f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04b8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04b8f-105">16 進数の文字列表現の指定された部分を 2 進数に変換します。</span><span class="sxs-lookup"><span data-stu-id="04b8f-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04b8f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="04b8f-106">Header file:</span></span>  <br/> |<span data-ttu-id="04b8f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="04b8f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="04b8f-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="04b8f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="04b8f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="04b8f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="04b8f-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="04b8f-110">Called by:</span></span>  <br/> |<span data-ttu-id="04b8f-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="04b8f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="04b8f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04b8f-112">Parameters</span></span>

 <span data-ttu-id="04b8f-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="04b8f-113">_sz_</span></span>
  
> <span data-ttu-id="04b8f-114">[in]変換する null 終端文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="04b8f-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="04b8f-115">有効な文字には、0 ~ 9 の 16 進文字と、大文字と小文字の両方の文字 a ~ f が含まれます。</span><span class="sxs-lookup"><span data-stu-id="04b8f-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="04b8f-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="04b8f-116">_pb_</span></span>
  
> <span data-ttu-id="04b8f-117">[out]返されるバイナリ番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="04b8f-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="04b8f-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="04b8f-118">_cb_</span></span>
  
> <span data-ttu-id="04b8f-119">[in]  _pb_ パラメーターのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="04b8f-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="04b8f-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="04b8f-120">Return value</span></span>

<span data-ttu-id="04b8f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="04b8f-121">S_OK</span></span>
  
> <span data-ttu-id="04b8f-122">変換が成功しました。</span><span class="sxs-lookup"><span data-stu-id="04b8f-122">Conversion was successful.</span></span>
    
<span data-ttu-id="04b8f-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="04b8f-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="04b8f-124">無効な文字が検出されました。</span><span class="sxs-lookup"><span data-stu-id="04b8f-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04b8f-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="04b8f-125">See also</span></span>



[<span data-ttu-id="04b8f-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="04b8f-126">FBinFromHex</span></span>](fbinfromhex.md)

