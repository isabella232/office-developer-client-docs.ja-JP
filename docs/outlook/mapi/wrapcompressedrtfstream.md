---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439801"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="81fcd-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="81fcd-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="81fcd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81fcd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81fcd-105">**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティで使用される圧縮形式から、圧縮されていないリッチテキスト形式 (RTF) でテキストストリームを作成します。</span><span class="sxs-lookup"><span data-stu-id="81fcd-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81fcd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="81fcd-106">Header file:</span></span>  <br/> |<span data-ttu-id="81fcd-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81fcd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="81fcd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="81fcd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="81fcd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="81fcd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="81fcd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="81fcd-110">Called by:</span></span>  <br/> |<span data-ttu-id="81fcd-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="81fcd-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="81fcd-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81fcd-112">Parameters</span></span>

 <span data-ttu-id="81fcd-113">_lp圧縮 sedrtfstream_</span><span class="sxs-lookup"><span data-stu-id="81fcd-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="81fcd-114">順番メッセージの PR_RTF_COMPRESSED プロパティで開いているストリームへのポインター。</span><span class="sxs-lookup"><span data-stu-id="81fcd-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="81fcd-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81fcd-115">_ulFlags_</span></span>
  
> <span data-ttu-id="81fcd-116">順番関数のオプションフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="81fcd-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="81fcd-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="81fcd-117">The following flags can be set:</span></span>
    
<span data-ttu-id="81fcd-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="81fcd-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="81fcd-119">クライアントが、返されるラップされた stream インターフェイスの読み取りまたは書き込みを行うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="81fcd-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="81fcd-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="81fcd-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="81fcd-121">非圧縮 RTF は、lpな形式のストリームに__ 書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="81fcd-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="81fcd-122">_lp非暗号化 sedrtfstream_</span><span class="sxs-lookup"><span data-stu-id="81fcd-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="81fcd-123">読み上げ**WrapCompressedRTFStream**が圧縮されていない RTF のストリームを返す場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="81fcd-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="81fcd-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="81fcd-124">Return value</span></span>

<span data-ttu-id="81fcd-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="81fcd-125">S_OK</span></span> 
  
> <span data-ttu-id="81fcd-126">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="81fcd-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81fcd-127">注釈</span><span class="sxs-lookup"><span data-stu-id="81fcd-127">Remarks</span></span>

<span data-ttu-id="81fcd-128">MAPI_MODIFY フラグが_ulflags_パラメーターに渡されている場合、 _lp sedrtfstream_パラメーターは、読み取りおよび書き込みのために既に開いている必要があります。</span><span class="sxs-lookup"><span data-stu-id="81fcd-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="81fcd-129">新しい、非圧縮 RTF テキストは、lp、暗号化されていない_sedrtfストリーム_で返される stream インターフェイスに書き込まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="81fcd-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="81fcd-130">既存のストリームを追加することはできないため、メッセージテキスト全体を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81fcd-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="81fcd-131">_ulflags_パラメーターに0が渡された場合、 _lp圧縮 sedrtfstream_を読み取り専用で開くことができます。</span><span class="sxs-lookup"><span data-stu-id="81fcd-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="81fcd-132">lpout の出力によって返されるストリームインターフェイスからは、メッセージ__ テキスト全体のみを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="81fcd-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="81fcd-133">ストリームの途中から検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="81fcd-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="81fcd-134">**WrapCompressedRTFStream**は、圧縮ストリームのポインターがストリームの先頭に設定されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="81fcd-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="81fcd-135">特定の OLE **IStream**メソッドは、返される非圧縮ストリームではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="81fcd-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="81fcd-136">**IStream:: Clone**、 **istream:: lockregion**、 **istream:: Revert**、 **istream:: Seek**、istream: **: SetSize**、 **istream:: Stat**、および**istream:: UnlockRegion**が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81fcd-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="81fcd-137">ストリーム全体にコピーするためには、読み取り/書き込みループが必要です。</span><span class="sxs-lookup"><span data-stu-id="81fcd-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="81fcd-138">クライアントは新しい RTF を圧縮されていない形式で書き込むので、ストリームに直接書き込むのではなく、 **WrapCompressedRTFStream**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81fcd-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="81fcd-139">RTF 対応クライアントは、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで STORE_UNCOMPRESSED_RTF フラグを検索し、設定されている場合は**WrapCompressed RTFStream**に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="81fcd-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81fcd-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="81fcd-140">See also</span></span>



[<span data-ttu-id="81fcd-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="81fcd-141">RTFSync</span></span>](rtfsync.md)

