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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723034"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="b8974-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="b8974-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="b8974-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8974-105">MIME ストリームを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="b8974-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="b8974-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b8974-106">Parameters</span></span>

 <span data-ttu-id="b8974-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="b8974-107">_pstm_</span></span>
  
> <span data-ttu-id="b8974-108">[in]MIME ストリームの[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="b8974-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="b8974-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="b8974-109">_pmsg_</span></span>
  
> <span data-ttu-id="b8974-110">[out]ロードするのには、メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b8974-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="b8974-111">**LPMESSAGE**の型定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8974-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="b8974-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="b8974-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="b8974-113">[in]この値を**null**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8974-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="b8974-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8974-114">_ulFlags_</span></span>
  
> <span data-ttu-id="b8974-115">[in]このパラメーターは、変換中に実行される特別な操作を識別します。</span><span class="sxs-lookup"><span data-stu-id="b8974-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="b8974-116">ゼロ (0) を実行するには、特定のアクションがない場合、または次の値の組み合わせである必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8974-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="b8974-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="b8974-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="b8974-118">未送信の X で送信された未送信の情報が保持されます。</span><span class="sxs-lookup"><span data-stu-id="b8974-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="b8974-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="b8974-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="b8974-120">MIME ストリームでは、簡易 MAPI 転送プロトコル (SMTP) メッセージです。</span><span class="sxs-lookup"><span data-stu-id="b8974-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="b8974-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="b8974-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="b8974-122">MIME ストリームの BCC 受信者が MAPI メッセージに含まれます。</span><span class="sxs-lookup"><span data-stu-id="b8974-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="b8974-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="b8974-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="b8974-124">MAPI メッセージの MIME ストリームの HTML 本文をリッチ テキスト形式 (RTF) に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8974-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="b8974-125">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="b8974-125">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="b8974-126">コンバーターでは、国際メッセージ (EAI/RFC6530) として MIME ストリームを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8974-126">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="b8974-127">Outlook 2013 でサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b8974-127">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8974-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="b8974-128">Return value</span></span>

<span data-ttu-id="b8974-129">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b8974-129">E_INVALIDARG</span></span>
  
> <span data-ttu-id="b8974-130">_Pstm_が**null**こと、 _pmsg_が**null**、または、 _ulFlags_が有効ではありませんを示します。</span><span class="sxs-lookup"><span data-stu-id="b8974-130">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b8974-131">注釈</span><span class="sxs-lookup"><span data-stu-id="b8974-131">Remarks</span></span>

<span data-ttu-id="b8974-132">_UlFlags_の一部として**CCSF_USE_RTF**を指定した送信先メッセージ ・ ストアが HTML や rtf 形式の両方をサポートしている場合は、MAPI メッセージは、html 形式または rtf 形式に変換されます。</span><span class="sxs-lookup"><span data-stu-id="b8974-132">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="b8974-133">変換後のフォーマットを圧縮する場合は、メッセージを rtf 形式に変換すると、rtf 形式、HTML は、圧縮された RTF 文字列に埋め込まれ、 [PidTagRtfCompressed の標準的なプロパティ](pidtagrtfcompressed-canonical-property.md)に文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b8974-133">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8974-134">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b8974-134">MFCMAPI reference</span></span>

<span data-ttu-id="b8974-135">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8974-135">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8974-136">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b8974-136">**File**</span></span>|<span data-ttu-id="b8974-137">**関数**</span><span class="sxs-lookup"><span data-stu-id="b8974-137">**Function**</span></span>|<span data-ttu-id="b8974-138">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b8974-138">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8974-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="b8974-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="b8974-140">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="b8974-140">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="b8974-141">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="b8974-141">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="b8974-142">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="b8974-142">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="b8974-143">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="b8974-143">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="b8974-144">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="b8974-144">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8974-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8974-145">See also</span></span>



[<span data-ttu-id="b8974-146">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8974-146">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="b8974-147">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="b8974-147">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="b8974-148">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="b8974-148">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="b8974-149">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="b8974-149">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="b8974-150">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="b8974-150">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="b8974-151">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="b8974-151">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="b8974-152">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="b8974-152">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="b8974-153">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="b8974-153">MAPI Constants</span></span>](mapi-constants.md)

