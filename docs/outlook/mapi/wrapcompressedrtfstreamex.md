---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325775"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="e178f-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="e178f-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="e178f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e178f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e178f-105">圧縮リッチ テキスト形式 (RTF) の電子メール メッセージの本文を圧縮解除し、圧縮解除されたストリームの形式を示し、必要に応じて圧縮解除されたストリームをネイティブ形式に変換し、圧縮解除されたストリームまたは変換されたネイティブ ストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="e178f-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e178f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e178f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e178f-107">次の方法でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="e178f-107">Exported by:</span></span>  <br/> |<span data-ttu-id="e178f-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e178f-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="e178f-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e178f-109">Called by:</span></span>  <br/> |<span data-ttu-id="e178f-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="e178f-110">Client</span></span>  <br/> |
|<span data-ttu-id="e178f-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="e178f-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e178f-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="e178f-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="e178f-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e178f-113">Parameters</span></span>

<span data-ttu-id="e178f-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="e178f-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="e178f-115">[in]これは、メッセージの [PidTagRtfCompressed Canonical プロパティ](pidtagrtfcompressed-canonical-property.md) で開くストリームへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="e178f-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="e178f-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="e178f-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="e178f-117">[in]これは、a を指すポインターです。</span><span class="sxs-lookup"><span data-stu-id="e178f-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="e178f-118">[RTF_WCSINFO](rtf_wcsinfo.md) オプションを含む構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="e178f-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="e178f-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="e178f-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="e178f-120">[out]これは、圧縮解除された RTF のストリームが返される場所へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="e178f-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="e178f-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="e178f-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="e178f-122">[out]これは、返される圧縮解除 [されたRTF_WCSRETINFO](rtf_wcsretinfo.md) 形式に関する情報を含むオブジェクト構造へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="e178f-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e178f-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="e178f-123">Return values</span></span>

<span data-ttu-id="e178f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e178f-124">S_OK</span></span> 
  
- <span data-ttu-id="e178f-125">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="e178f-125">The function call is successful.</span></span>
    
<span data-ttu-id="e178f-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e178f-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="e178f-127">これは *、pWCSInfo* が指す **RTF_WCSINFO** 構造体の **ulFlags** フィールドの **MAPI_MODIFY** フラグと MAPI_NATIVE_BODY フラグを組み合 **わせた** 場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="e178f-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e178f-128">注釈</span><span class="sxs-lookup"><span data-stu-id="e178f-128">Remarks</span></span>

<span data-ttu-id="e178f-129">**WrapCompressedRTFStreamEx** を使用すると、ストリームを解凍して圧縮された RTF にカプセル化された電子メール メッセージの本文にアクセスし、圧縮解除されたストリームとその形式、およびオプションでネイティブ本文ストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="e178f-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="e178f-130">ネイティブ本文ストリームは、RTF、プレーン テキスト、または HTML で指定できます。</span><span class="sxs-lookup"><span data-stu-id="e178f-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="e178f-131">オブジェクト Microsoft Office Outlookは **、MailItem** オブジェクトの Body プロパティと、本文テキストの形式を示す [MailItem.BodyFormat プロパティ (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx)を提供します。</span><span class="sxs-lookup"><span data-stu-id="e178f-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="e178f-132">設計上、セキュリティ ガードによって信頼されていないソリューションは、Outlook Security Guard によって生成されたセキュリティ ダイアログ ボックスOutlook呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e178f-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="e178f-133">エクスポートされた MAPI 関数 **WrapCompressedRTFStreamEx** を使用すると、ソリューションは Outlook オブジェクト モデルではなく MAPI を使用し、これらのセキュリティ ダイアログ ボックスを回避できます。</span><span class="sxs-lookup"><span data-stu-id="e178f-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="e178f-134">MAPI **\_ NATIVE_BODY** フラグを *pWCSInfo* が指す **RTF \_ WCSINFO** 構造体の **ulFlags** フィールドの **MAPI \_ MODIFY** フラグと組み合わせはできないので、読み取り専用モードでのみネイティブ本文ストリームにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e178f-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="e178f-135">読み取り/書き込みモードでネイティブ本文ストリームにアクセスするには **、WrapCompressedRTFStream 関数を使用する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="e178f-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e178f-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="e178f-136">See also</span></span>

- [<span data-ttu-id="e178f-137">圧縮 RTF でメッセージの本文を取得し、それをネイティブ形式に変換する</span><span class="sxs-lookup"><span data-stu-id="e178f-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

