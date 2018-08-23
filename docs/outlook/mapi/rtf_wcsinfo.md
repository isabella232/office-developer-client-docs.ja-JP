---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c328e79b7e474369f11f8a4002e00137659db3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803806"
---
# <a name="rtfwcsinfo"></a><span data-ttu-id="16c17-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="16c17-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="16c17-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16c17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16c17-105">この構造体を使用すると、圧縮されたリッチ テキスト形式 (RTF) でメッセージの本文を圧縮解除し、必要に応じて、ネイティブ形式で本文のストリームを返すのための情報を指定できます。</span><span class="sxs-lookup"><span data-stu-id="16c17-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="16c17-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="16c17-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="16c17-107">Members</span><span class="sxs-lookup"><span data-stu-id="16c17-107">Members</span></span>

 <span data-ttu-id="16c17-108">_size_</span><span class="sxs-lookup"><span data-stu-id="16c17-108">_size_</span></span>
  
> <span data-ttu-id="16c17-109">バイト数**について**の構造体のサイズです。</span><span class="sxs-lookup"><span data-stu-id="16c17-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="16c17-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="16c17-110">_ulFlags_</span></span>
  
> <span data-ttu-id="16c17-111">[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数のオプション フラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="16c17-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="16c17-112">サポートされているオプションのフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="16c17-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="16c17-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="16c17-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="16c17-114">これは、クライアントが返されたラップされたストリーム インターフェイスを作成しようとしたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="16c17-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="16c17-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="16c17-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="16c17-116">これは、圧縮解除された RTF を[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数の_lpCompressedRTFStream_ポインターによりポイントされているストリームに書き込まれることになっているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="16c17-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="16c17-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="16c17-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="16c17-118">これは、ストリームを返す前に、ネイティブ形式の本文を圧縮解除されたストリームも変換かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="16c17-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="16c17-119">**MAPI_MODIFY**フラグでこのフラグを組み合わせることはできません。</span><span class="sxs-lookup"><span data-stu-id="16c17-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="16c17-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="16c17-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="16c17-121">これは、メッセージのコード ページ値です。</span><span class="sxs-lookup"><span data-stu-id="16c17-121">This is the code page value of the message.</span></span> <span data-ttu-id="16c17-122">通常、この値は、メッセージの[PidTagInternetCodepage の標準的なプロパティ](pidtaginternetcodepage-canonical-property.md)から取得されます。</span><span class="sxs-lookup"><span data-stu-id="16c17-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="16c17-123">_UlFlags_に**MAPI_NATIVE_BODY**フラグが渡された場合、この値はのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="16c17-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="16c17-124">それ以外の場合、この値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="16c17-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="16c17-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="16c17-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="16c17-126">これは、使用する返された圧縮解除ストリームのコード ページの値です。</span><span class="sxs-lookup"><span data-stu-id="16c17-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="16c17-127">これは、0 以外の値に設定されている場合、 [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)関数は、ストリームを指定したコード ページに変換します。</span><span class="sxs-lookup"><span data-stu-id="16c17-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="16c17-128">値がゼロに設定すると、MAPI は、使用するコード ページを決定します。</span><span class="sxs-lookup"><span data-stu-id="16c17-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="16c17-129">_UlFlags_、 **MAPI_NATIVE_BODY**フラグが渡され、本文が RTF でない場合にのみ、この値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="16c17-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="16c17-130">それ以外の場合、この値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="16c17-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16c17-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="16c17-131">See also</span></span>



[<span data-ttu-id="16c17-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="16c17-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

