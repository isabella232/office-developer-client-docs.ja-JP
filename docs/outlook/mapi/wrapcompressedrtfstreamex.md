---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391732"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="6ffcb-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="6ffcb-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="6ffcb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ffcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ffcb-105">圧縮解除で圧縮されたリッチ テキスト形式式 (RTF)、電子メール メッセージの本文圧縮解除ストリームの形式を指定、必要に応じてネイティブ形式、圧縮解除されたストリームに変換し、いずれかの圧縮解除されたストリームを返しますまたは、。ネイティブ ストリームを変換します。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6ffcb-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="6ffcb-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ffcb-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-107">Exported by:</span></span>  <br/> |<span data-ttu-id="6ffcb-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="6ffcb-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="6ffcb-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6ffcb-109">Called by:</span></span>  <br/> |<span data-ttu-id="6ffcb-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="6ffcb-110">Client</span></span>  <br/> |
|<span data-ttu-id="6ffcb-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="6ffcb-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="6ffcb-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="6ffcb-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="6ffcb-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6ffcb-113">Parameters</span></span>

<span data-ttu-id="6ffcb-114">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="6ffcb-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="6ffcb-115">[in]これは、メッセージの[既定のプロパティの PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)で開かれているストリームへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="6ffcb-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="6ffcb-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="6ffcb-117">[in]ポインターは、</span><span class="sxs-lookup"><span data-stu-id="6ffcb-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="6ffcb-118">関数のオプションを含む[について](rtf_wcsinfo.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="6ffcb-119">_lppUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="6ffcb-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="6ffcb-120">[out]これは、圧縮解除の rtf 形式のストリームが返される位置の場所へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="6ffcb-121">_pRetInfo_</span><span class="sxs-lookup"><span data-stu-id="6ffcb-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="6ffcb-122">[out]これは、返された圧縮解除ストリームの形式に関する情報が含まれている[この](rtf_wcsretinfo.md)構造体へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6ffcb-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="6ffcb-123">Return values</span></span>

<span data-ttu-id="6ffcb-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ffcb-124">S_OK</span></span> 
  
- <span data-ttu-id="6ffcb-125">関数の呼び出しが成功します。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-125">The function call is successful.</span></span>
    
<span data-ttu-id="6ffcb-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6ffcb-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="6ffcb-127">**MAPI_NATIVE_BODY**フラグは、 **ulFlags** 、**について**構造体のフィールドで示される*pWCSInfo*の**MAPI_MODIFY**フラグを使用している場合、この関数が返されます。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6ffcb-128">備考</span><span class="sxs-lookup"><span data-stu-id="6ffcb-128">Remarks</span></span>

<span data-ttu-id="6ffcb-129">**WrapCompressedRTFStreamEx**は、ストリームを圧縮解除、圧縮された rtf 形式でカプセル化された電子メール メッセージの本文にアクセスできるように、圧縮解除されたストリームの形式では、および必要に応じてネイティブ形式の本文のストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="6ffcb-130">ネイティブ形式の本文のストリームは、RTF、プレーン テキスト、または HTML で指定できます。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="6ffcb-131">Microsoft Office Outlook オブジェクト モデルでは、 **MailItem**オブジェクトおよび本文テキストの書式を示す[MailItem.BodyFormat プロパティ (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx)の**本文**のプロパティを提供します。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="6ffcb-132">仕様では、Outlook で信頼されていないソリューションは、セキュリティに関するダイアログ ボックスで Outlook セキュリティ ガードの生成を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="6ffcb-133">エクスポートされた MAPI 関数**WrapCompressedRTFStreamEx**を使用すると、MAPI を使用して、Outlook オブジェクト モデルではなく、これらのセキュリティ] ダイアログ ボックスを回避するソリューションができます。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="6ffcb-134">**MAPI\_NATIVE_BODY**とフラグを組み合わせることはできません、 **MAPI\_変更**の**ulFlags**フィールドのフラグ、 **RTF\_WCSINFO** *pWCSInfo*が指す構造体のみを使用するネイティブ読み取り専用モードで本文のストリーム。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="6ffcb-135">読み取り/書き込みモードでのネイティブ形式の本文のストリームにアクセスするには、 **WrapCompressedRTFStream**関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ffcb-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ffcb-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ffcb-136">See also</span></span>

- [<span data-ttu-id="6ffcb-137">圧縮 RTF 内のメッセージ本体を取り出し、ネイティブ形式に変換する</span><span class="sxs-lookup"><span data-stu-id="6ffcb-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

