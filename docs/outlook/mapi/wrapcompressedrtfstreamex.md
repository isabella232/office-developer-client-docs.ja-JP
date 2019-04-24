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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325775"
---
# <a name="wrapcompressedrtfstreamex"></a><span data-ttu-id="5f04b-103">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="5f04b-103">WrapCompressedRTFStreamEx</span></span>

<span data-ttu-id="5f04b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f04b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f04b-105">圧縮されたリッチテキスト形式 (RTF) の電子メールメッセージの本文を伸張し、圧縮されていないストリームの形式を示し、必要に応じて圧縮解除したストリームをネイティブ形式に変換して、圧縮解除されたストリームまたはのいずれかを返します。変換されたネイティブストリーム。</span><span class="sxs-lookup"><span data-stu-id="5f04b-105">Decompresses the the body of an email message that is in compressed Rich Text Format (RTF), indicates the format of the decompressed stream, optionally converts the decompressed stream to its native format, and returns either the decompressed stream or the converted native stream.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5f04b-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5f04b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f04b-107">エクスポート対象:</span><span class="sxs-lookup"><span data-stu-id="5f04b-107">Exported by:</span></span>  <br/> |<span data-ttu-id="5f04b-108">msmapi32</span><span class="sxs-lookup"><span data-stu-id="5f04b-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="5f04b-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5f04b-109">Called by:</span></span>  <br/> |<span data-ttu-id="5f04b-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="5f04b-110">Client</span></span>  <br/> |
|<span data-ttu-id="5f04b-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="5f04b-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5f04b-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="5f04b-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a><span data-ttu-id="5f04b-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5f04b-113">Parameters</span></span>

<span data-ttu-id="5f04b-114">_lp圧縮 sedrtfstream_</span><span class="sxs-lookup"><span data-stu-id="5f04b-114">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="5f04b-115">順番これは、メッセージの[PidTagRtfCompressed 標準プロパティ](pidtagrtfcompressed-canonical-property.md)で開かれるストリームへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="5f04b-115">[in] This is a pointer to a stream that is opened on the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md) of a message.</span></span> 
    
<span data-ttu-id="5f04b-116">_pWCSInfo_</span><span class="sxs-lookup"><span data-stu-id="5f04b-116">_pWCSInfo_</span></span>
  
> <span data-ttu-id="5f04b-117">順番これは、</span><span class="sxs-lookup"><span data-stu-id="5f04b-117">[in] This is a pointer to a</span></span> 
    
   <span data-ttu-id="5f04b-118">関数のオプションを含む[RTF_WCSINFO](rtf_wcsinfo.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="5f04b-118">[RTF_WCSINFO](rtf_wcsinfo.md) structure that contains options for the function.</span></span> 
    
<span data-ttu-id="5f04b-119">_lpp非圧縮 sedrtfstream_</span><span class="sxs-lookup"><span data-stu-id="5f04b-119">_lppUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="5f04b-120">読み上げこれは、解凍された RTF のストリームが返される場所へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="5f04b-120">[out] This is a pointer to the location where a stream for the decompressed RTF is returned.</span></span> 
    
<span data-ttu-id="5f04b-121">_この情報_</span><span class="sxs-lookup"><span data-stu-id="5f04b-121">_pRetInfo_</span></span>
  
> <span data-ttu-id="5f04b-122">読み上げこれは、返された圧縮解除ストリームの形式に関する情報を含む[RTF_WCSRETINFO](rtf_wcsretinfo.md)構造体へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="5f04b-122">[out] This is a pointer to a [RTF_WCSRETINFO](rtf_wcsretinfo.md) structure that contains information about the format of the returned decompressed stream.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5f04b-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="5f04b-123">Return values</span></span>

<span data-ttu-id="5f04b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f04b-124">S_OK</span></span> 
  
- <span data-ttu-id="5f04b-125">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="5f04b-125">The function call is successful.</span></span>
    
<span data-ttu-id="5f04b-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5f04b-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
- <span data-ttu-id="5f04b-127">これは、 **MAPI_NATIVE_BODY**フラグが*pWCSInfo*で示される**RTF_WCSINFO**構造の**ulflags**フィールドの**MAPI_MODIFY**フラグと組み合わされている場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="5f04b-127">This is returned if the **MAPI_NATIVE_BODY** flag is combined with the **MAPI_MODIFY** flag in the **ulFlags** field of the **RTF_WCSINFO** structure pointed at by  *pWCSInfo*  .</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5f04b-128">解説</span><span class="sxs-lookup"><span data-stu-id="5f04b-128">Remarks</span></span>

<span data-ttu-id="5f04b-129">**WrapCompressedRTFStreamEx**では、ストリームを解凍することで、圧縮された RTF でカプセル化された電子メールメッセージの本文にアクセスし、圧縮解除されたストリームとその形式、および必要に応じてネイティブ本文ストリームを返します。</span><span class="sxs-lookup"><span data-stu-id="5f04b-129">**WrapCompressedRTFStreamEx** allows you to access the body of an email message encapsulated in compressed RTF by decompressing the stream, returns the decompressed stream and its format, and optionally the native body stream.</span></span> <span data-ttu-id="5f04b-130">ネイティブ本文のストリームは、RTF、プレーンテキスト、または HTML のいずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5f04b-130">The native body stream can be in RTF, plain text, or HTML.</span></span> 
  
<span data-ttu-id="5f04b-131">Microsoft Office Outlook オブジェクトモデルには、 **mailitem**オブジェクトの**body**プロパティと、本文テキストの形式を示す[BodyFormat プロパティ (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx)が用意されています。</span><span class="sxs-lookup"><span data-stu-id="5f04b-131">The Microsoft Office Outlook object model provides a **Body** property for **MailItem** objects and a [MailItem.BodyFormat Property (Outlook)](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) that indicates the format of the body text.</span></span> <span data-ttu-id="5f04b-132">設計上、outlook によって信頼されていないソリューションは、outlook セキュリティガードによって生成されるセキュリティダイアログボックスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5f04b-132">By design, a solution that is not trusted by Outlook invokes security dialog boxes generated by the Outlook Security Guard.</span></span> <span data-ttu-id="5f04b-133">エクスポートされた mapi 関数**WrapCompressedRTFStreamEx**を使用すると、ソリューションは Outlook オブジェクトモデルではなく mapi を使用し、これらのセキュリティダイアログボックスを回避することができます。</span><span class="sxs-lookup"><span data-stu-id="5f04b-133">Using the exported MAPI function **WrapCompressedRTFStreamEx** allows a solution to use MAPI instead of the Outlook object model and avoid these security dialog boxes.</span></span> 
  
<span data-ttu-id="5f04b-134">**mapi\_NATIVE_BODY**フラグは、 *pWCSInfo*によって参照されている**\_RTF WCSINFO**構造の**ulflags**フィールドに**mapi\_の変更**フラグと組み合わせて使用することはできないため、ネイティブのみにアクセスできます。読み取り専用モードの本文ストリーム。</span><span class="sxs-lookup"><span data-stu-id="5f04b-134">Because the **MAPI\_NATIVE_BODY** flag cannot be combined with the **MAPI\_MODIFY** flag in the **ulFlags** field of the **RTF\_WCSINFO** structure pointed at by *pWCSInfo*, you can only access the native body stream in read-only mode.</span></span> <span data-ttu-id="5f04b-135">読み取り/書き込みモードでネイティブ本文ストリームにアクセスするには、 **WrapCompressedRTFStream**関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f04b-135">To access the native body stream in read/write mode, you should use the **WrapCompressedRTFStream** function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f04b-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f04b-136">See also</span></span>

- [<span data-ttu-id="5f04b-137">圧縮 RTF でメッセージの本文を取得し、それをネイティブ形式に変換する</span><span class="sxs-lookup"><span data-stu-id="5f04b-137">Retrieve the Body of a Message in Compressed RTF and Convert It to Its Native Format</span></span>](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

