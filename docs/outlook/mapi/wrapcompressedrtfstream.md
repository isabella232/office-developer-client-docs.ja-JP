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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a7095907a1fb437e225922d0bef08b4ad79a4b6f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594594"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="5998a-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="5998a-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="5998a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5998a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5998a-105">圧縮されていない形式 (リッチ テキスト) ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) である**PR_RTF_COMPRESSED**プロパティで使用されている圧縮形式からテキストのストリームを作成します。</span><span class="sxs-lookup"><span data-stu-id="5998a-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5998a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5998a-106">Header file:</span></span>  <br/> |<span data-ttu-id="5998a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5998a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5998a-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="5998a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5998a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5998a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5998a-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5998a-110">Called by:</span></span>  <br/> |<span data-ttu-id="5998a-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5998a-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="5998a-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5998a-112">Parameters</span></span>

 <span data-ttu-id="5998a-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="5998a-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="5998a-114">[in]メッセージの PR_RTF_COMPRESSED プロパティで開かれているストリームへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5998a-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="5998a-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5998a-115">_ulFlags_</span></span>
  
> <span data-ttu-id="5998a-116">[in]関数のオプション フラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5998a-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="5998a-117">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5998a-117">The following flags can be set:</span></span>
    
<span data-ttu-id="5998a-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5998a-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5998a-119">かどうか、クライアントでは、読み取りまたは返されたラップされたストリーム インターフェイスを作成する予定です。</span><span class="sxs-lookup"><span data-stu-id="5998a-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="5998a-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="5998a-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="5998a-121">非圧縮の rtf 形式は、 _lpCompressedRTFStream_で示されるストリームに書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="5998a-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="5998a-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="5998a-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="5998a-123">[out]**WrapCompressedRTFStream**が非圧縮の rtf 形式のストリームを返す場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5998a-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5998a-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5998a-124">Return value</span></span>

<span data-ttu-id="5998a-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="5998a-125">S_OK</span></span> 
  
> <span data-ttu-id="5998a-126">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5998a-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5998a-127">����</span><span class="sxs-lookup"><span data-stu-id="5998a-127">Remarks</span></span>

<span data-ttu-id="5998a-128">MAPI_MODIFY フラグが渡された場合、 _ulFlags_パラメーターで、 _lpCompressedRTFStream_パラメーター必要があります読み取りおよび書き込み用に開かれています。</span><span class="sxs-lookup"><span data-stu-id="5998a-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="5998a-129">Rtf 形式のテキストが圧縮されていない、新しいは、 _lpUncompressedRTFStream_で返されるストリームのインタ フェースに書き込まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5998a-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="5998a-130">既存のストリームを追加することはできません、ため、メッセージ テキスト全体を書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="5998a-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="5998a-131">_UlFlags_パラメーターに 0 を渡した場合、 _lpCompressedRTFStream_開くことができます読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="5998a-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="5998a-132">_LpUncompressedRTFStream_で返されるストリームのインタ フェースからのみ、メッセージ テキスト全体を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="5998a-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="5998a-133">ストリームの中間の開始を検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="5998a-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="5998a-134">**WrapCompressedRTFStream**では、圧縮されたストリームのポインターをストリームの先頭に設定されていると仮定しています。</span><span class="sxs-lookup"><span data-stu-id="5998a-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="5998a-135">返された圧縮解除されたストリームでは、特定の OLE **IStream**のメソッドはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5998a-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="5998a-136">**IStream::Clone**、 **IStream::LockRegion**、 **IStream::Revert**、 **IStream::Seek**、 **IStream::SetSize**、 **IStream::Stat**、および**IStream::UnlockRegion**が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5998a-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="5998a-137">ストリーム全体をコピーするために読み取り/書き込みループが必要です。</span><span class="sxs-lookup"><span data-stu-id="5998a-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="5998a-138">クライアントが圧縮されていない形式で新しい RTF を書き込むためのストリームに直接書き込むのではなく、 **WrapCompressedRTFStream**を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5998a-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="5998a-139">RTF に対応していないクライアントは、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティに STORE_UNCOMPRESSED_RTF フラグを検索し、設定されている場合に、 **WrapCompressed RTFStream**に渡すこと必要があります。</span><span class="sxs-lookup"><span data-stu-id="5998a-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5998a-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="5998a-140">See also</span></span>



[<span data-ttu-id="5998a-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="5998a-141">RTFSync</span></span>](rtfsync.md)

