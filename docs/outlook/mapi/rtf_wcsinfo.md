---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430533"
---
# <a name="rtf_wcsinfo"></a><span data-ttu-id="64c8d-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="64c8d-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="64c8d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64c8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64c8d-105">この構造を使用すると、圧縮リッチ テキスト形式 (RTF) でメッセージの本文を解凍する情報を指定し、必要に応じて本文ストリームをネイティブ形式で返します。</span><span class="sxs-lookup"><span data-stu-id="64c8d-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="64c8d-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="64c8d-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="64c8d-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="64c8d-107">Members</span></span>

 <span data-ttu-id="64c8d-108">_size_</span><span class="sxs-lookup"><span data-stu-id="64c8d-108">_size_</span></span>
  
> <span data-ttu-id="64c8d-109">構造体のサイズ **RTF_WCSINFO** バイト数で指定します。</span><span class="sxs-lookup"><span data-stu-id="64c8d-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="64c8d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="64c8d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="64c8d-111">これは [、WrapCompressedRTFStreamEx 関数](wrapcompressedrtfstreamex.md) のオプション フラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="64c8d-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="64c8d-112">サポートされているオプション フラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="64c8d-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="64c8d-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="64c8d-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="64c8d-114">これは、クライアントが返されるラップされたストリーム インターフェイスを書き込むかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="64c8d-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="64c8d-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="64c8d-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="64c8d-116">これは [、WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数の _lpCompressedRTFStream_ ポインターによって指されるストリームに、圧縮解除された RTF を書き込むかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="64c8d-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="64c8d-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="64c8d-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="64c8d-118">これは、圧縮解除されたストリームも、ストリームを返す前にネイティブ本文に変換されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="64c8d-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="64c8d-119">このフラグは、このフラグと組 **み合MAPI_MODIFY** できません。</span><span class="sxs-lookup"><span data-stu-id="64c8d-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="64c8d-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="64c8d-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="64c8d-121">これは、メッセージのコード ページ値です。</span><span class="sxs-lookup"><span data-stu-id="64c8d-121">This is the code page value of the message.</span></span> <span data-ttu-id="64c8d-122">通常、この値は、メッセージの [PidTagInternetCodepage 標準プロパティ](pidtaginternetcodepage-canonical-property.md) から取得されます。</span><span class="sxs-lookup"><span data-stu-id="64c8d-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="64c8d-123">この値は、ulFlags **でMAPI_NATIVE_BODYフラグ** が渡される  _場合にのみ使用されます_。</span><span class="sxs-lookup"><span data-stu-id="64c8d-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="64c8d-124">それ以外の場合、この値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="64c8d-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="64c8d-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="64c8d-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="64c8d-126">これは、必要な、返される圧縮解除ストリームのコード ページ値です。</span><span class="sxs-lookup"><span data-stu-id="64c8d-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="64c8d-127">これが 0 以外の値に設定されている場合 [、WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) 関数はストリームを指定したコード ページに変換します。</span><span class="sxs-lookup"><span data-stu-id="64c8d-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="64c8d-128">これがゼロ値に設定されている場合、MAPI は使用するコード ページを決定します。</span><span class="sxs-lookup"><span data-stu-id="64c8d-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="64c8d-129">この値は、MAPI_NATIVE_BODYフラグ **が**  _ulFlags_ で渡され、本文形式が RTF ではない場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="64c8d-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="64c8d-130">それ以外の場合、この値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="64c8d-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64c8d-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="64c8d-131">See also</span></span>



[<span data-ttu-id="64c8d-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="64c8d-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

