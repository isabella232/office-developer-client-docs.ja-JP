---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326930"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="86f1f-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="86f1f-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="86f1f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86f1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86f1f-105">MIME ストリームを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="86f1f-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="86f1f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="86f1f-106">Parameters</span></span>

 <span data-ttu-id="86f1f-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="86f1f-107">_pstm_</span></span>
  
> <span data-ttu-id="86f1f-108">順番MIME ストリームへの[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="86f1f-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="86f1f-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="86f1f-109">_pmsg_</span></span>
  
> <span data-ttu-id="86f1f-110">読み上げ読み込むメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="86f1f-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="86f1f-111">**lpmessage**の種類の定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86f1f-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="86f1f-112">_pszsrcsrv_</span><span class="sxs-lookup"><span data-stu-id="86f1f-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="86f1f-113">順番この値は**null**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="86f1f-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="86f1f-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="86f1f-114">_ulFlags_</span></span>
  
> <span data-ttu-id="86f1f-115">順番このパラメーターには、変換中に実行する特別なアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="86f1f-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="86f1f-116">特定のアクションを実行する必要がない場合、または次の値の組み合わせを指定する場合は、ゼロ (0) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="86f1f-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="86f1f-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="86f1f-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="86f1f-118">送信/未送信の情報は、X 未送信の情報として保持されます。</span><span class="sxs-lookup"><span data-stu-id="86f1f-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="86f1f-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="86f1f-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="86f1f-120">MIME ストリームは、簡易 MAPI 転送プロトコル (SMTP) メッセージのためのものです。</span><span class="sxs-lookup"><span data-stu-id="86f1f-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="86f1f-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="86f1f-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="86f1f-122">MIME ストリームの BCC 受信者は、MAPI メッセージに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="86f1f-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="86f1f-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="86f1f-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="86f1f-124">MIME ストリームの HTML 本文は、MAPI メッセージでリッチテキスト形式 (RTF) に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86f1f-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="86f1f-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="86f1f-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="86f1f-126">コンバータは、MIME ストリームを国際メッセージ (EAI/RFC6530) として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86f1f-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="86f1f-127">Outlook 2013 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="86f1f-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="86f1f-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="86f1f-128">Return value</span></span>

<span data-ttu-id="86f1f-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="86f1f-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="86f1f-130">_pstm_が**null**、 _pmsg_が**null**、 _ulflags_が無効であることを示します。</span><span class="sxs-lookup"><span data-stu-id="86f1f-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86f1f-131">解説</span><span class="sxs-lookup"><span data-stu-id="86f1f-131">Remarks</span></span>

<span data-ttu-id="86f1f-132">**CCSF_USE_RTF**を_ulflags_の一部として指定して、宛先メッセージストアが html と rtf の両方をサポートしている場合、MAPI メッセージは html または rtf に変換されます。</span><span class="sxs-lookup"><span data-stu-id="86f1f-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="86f1f-133">メッセージが rtf に変換される場合、変換された形式は rtf 形式に変換され、すべての HTML が圧縮 rtf 文字列に埋め込まれ、文字列が[PidTagRtfCompressed 標準プロパティ](pidtagrtfcompressed-canonical-property.md)に格納されます。</span><span class="sxs-lookup"><span data-stu-id="86f1f-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="86f1f-134">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="86f1f-134">MFCMAPI reference</span></span>

<span data-ttu-id="86f1f-135">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="86f1f-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="86f1f-136">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="86f1f-136">**File**</span></span>|<span data-ttu-id="86f1f-137">**関数**</span><span class="sxs-lookup"><span data-stu-id="86f1f-137">**Function**</span></span>|<span data-ttu-id="86f1f-138">**コメント**</span><span class="sxs-lookup"><span data-stu-id="86f1f-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="86f1f-139">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="86f1f-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="86f1f-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="86f1f-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="86f1f-141">mfcmapi は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="86f1f-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="86f1f-142">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="86f1f-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="86f1f-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="86f1f-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="86f1f-144">mfcmapi は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="86f1f-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86f1f-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="86f1f-145">See also</span></span>



[<span data-ttu-id="86f1f-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86f1f-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="86f1f-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="86f1f-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="86f1f-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="86f1f-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="86f1f-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="86f1f-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="86f1f-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="86f1f-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="86f1f-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="86f1f-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="86f1f-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="86f1f-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="86f1f-153">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="86f1f-153">MAPI Constants</span></span>](mapi-constants.md)

