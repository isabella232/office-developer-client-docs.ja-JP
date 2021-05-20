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
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="103b0-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="103b0-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="103b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="103b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="103b0-105">PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティで使用される圧縮形式から、圧縮されていないリッチ テキスト形式 (RTF)**で** テキスト ストリームを作成します。</span><span class="sxs-lookup"><span data-stu-id="103b0-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="103b0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="103b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="103b0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="103b0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="103b0-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="103b0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="103b0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="103b0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="103b0-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="103b0-110">Called by:</span></span>  <br/> |<span data-ttu-id="103b0-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="103b0-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="103b0-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="103b0-112">Parameters</span></span>

 <span data-ttu-id="103b0-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="103b0-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="103b0-114">[in]メッセージの PR_RTF_COMPRESSEDで開いたストリームへのポインター。</span><span class="sxs-lookup"><span data-stu-id="103b0-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="103b0-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="103b0-115">_ulFlags_</span></span>
  
> <span data-ttu-id="103b0-116">[in]関数のオプション フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="103b0-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="103b0-117">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="103b0-117">The following flags can be set:</span></span>
    
<span data-ttu-id="103b0-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="103b0-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="103b0-119">クライアントが、返されるラップされたストリーム インターフェイスの読み取りまたは書き込みを行う場合。</span><span class="sxs-lookup"><span data-stu-id="103b0-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="103b0-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="103b0-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="103b0-121">圧縮されていない RTF は  _、lpCompressedRTFStream が指すストリームに書き込む必要があります_</span><span class="sxs-lookup"><span data-stu-id="103b0-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="103b0-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="103b0-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="103b0-123">[out] **WrapCompressedRTFStream** が非圧縮 RTF のストリームを返す場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="103b0-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="103b0-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="103b0-124">Return value</span></span>

<span data-ttu-id="103b0-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="103b0-125">S_OK</span></span> 
  
> <span data-ttu-id="103b0-126">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="103b0-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="103b0-127">注釈</span><span class="sxs-lookup"><span data-stu-id="103b0-127">Remarks</span></span>

<span data-ttu-id="103b0-128">_ulFlags_ パラメーター MAPI_MODIFYフラグが渡される場合 _、lpCompressedRTFStream_ パラメーターは読み取りおよび書き込みのために既に開いている必要があります。</span><span class="sxs-lookup"><span data-stu-id="103b0-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="103b0-129">lpUncompressedRTFStream で返されるストリーム インターフェイスに、圧縮されていない新しい RTF テキスト  _を書き込む必要があります_。</span><span class="sxs-lookup"><span data-stu-id="103b0-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="103b0-130">既存のストリームを追加できないので、メッセージ テキスト全体を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="103b0-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="103b0-131">_ulFlags_ パラメーターにゼロが渡された場合 _、lpCompressedRTFStream_ は読み取り専用で開くことができます。</span><span class="sxs-lookup"><span data-stu-id="103b0-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="103b0-132">_lpUncompressedRTFStream_ で返されるストリーム インターフェイスからメッセージ テキスト全体のみを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="103b0-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="103b0-133">ストリームの中央から検索はできません。</span><span class="sxs-lookup"><span data-stu-id="103b0-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="103b0-134">**WrapCompressedRTFStream** では、圧縮ストリームのポインターがストリームの先頭に設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="103b0-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="103b0-135">一部 **の OLE IStream** メソッドは、返される非圧縮ストリームではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="103b0-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="103b0-136">**IStream::Clone**、 **IStream::LockRegion**、 **IStream::Revert**、 **IStream::Seek**、 **IStream::SetSize**、 **IStream::Stat**、**および IStream::UnlockRegion** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="103b0-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="103b0-137">ストリーム全体にコピーするには、読み取り/書き込みループが必要です。</span><span class="sxs-lookup"><span data-stu-id="103b0-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="103b0-138">クライアントは、圧縮されていない形式で新しい RTF を書き込むため、ストリームに直接書き込む代わりに **WrapCompressedRTFStream** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="103b0-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="103b0-139">RTF 対応のクライアントは **、PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで STORE_UNCOMPRESSED_RTF フラグを検索し、それが設定されている場合は **WrapCompressed RTFStream** に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="103b0-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="103b0-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="103b0-140">See also</span></span>



[<span data-ttu-id="103b0-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="103b0-141">RTFSync</span></span>](rtfsync.md)

