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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357499"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="046f7-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="046f7-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="046f7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="046f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="046f7-105">16進数の文字列表現の指定した部分をバイナリ値に変換します。</span><span class="sxs-lookup"><span data-stu-id="046f7-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="046f7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="046f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="046f7-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="046f7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="046f7-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="046f7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="046f7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="046f7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="046f7-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="046f7-110">Called by:</span></span>  <br/> |<span data-ttu-id="046f7-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="046f7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="046f7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="046f7-112">Parameters</span></span>

 <span data-ttu-id="046f7-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="046f7-113">_sz_</span></span>
  
> <span data-ttu-id="046f7-114">順番変換する null で終わる文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="046f7-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="046f7-115">有効な文字には、0 ~ 9 の16進文字、大文字、小文字の a ~ f があります。</span><span class="sxs-lookup"><span data-stu-id="046f7-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="046f7-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="046f7-116">_pb_</span></span>
  
> <span data-ttu-id="046f7-117">読み上げ返されたバイナリ番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="046f7-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="046f7-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="046f7-118">_cb_</span></span>
  
> <span data-ttu-id="046f7-119">順番_pb_パラメーターのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="046f7-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="046f7-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="046f7-120">Return value</span></span>

<span data-ttu-id="046f7-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="046f7-121">S_OK</span></span>
  
> <span data-ttu-id="046f7-122">変換に成功しました。</span><span class="sxs-lookup"><span data-stu-id="046f7-122">Conversion was successful.</span></span>
    
<span data-ttu-id="046f7-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="046f7-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="046f7-124">無効な文字が検出されました。</span><span class="sxs-lookup"><span data-stu-id="046f7-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="046f7-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="046f7-125">See also</span></span>



[<span data-ttu-id="046f7-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="046f7-126">FBinFromHex</span></span>](fbinfromhex.md)

