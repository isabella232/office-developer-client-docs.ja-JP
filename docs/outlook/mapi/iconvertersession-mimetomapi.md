---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: '最終更新日: 2019 年9月6日'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160287"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="3f688-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="3f688-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="3f688-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f688-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f688-105">MIME ストリームを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="3f688-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="3f688-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3f688-106">Parameters</span></span>

 <span data-ttu-id="3f688-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="3f688-107">_pstm_</span></span>
  
> <span data-ttu-id="3f688-108">順番MIME ストリームへの[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="3f688-108">[in] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="3f688-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="3f688-109">_pmsg_</span></span>
  
> <span data-ttu-id="3f688-110">順番読み込むメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3f688-110">[in] Pointer to the message to load.</span></span> <span data-ttu-id="3f688-111">呼び出し元は、API に入力するメッセージを指定する必要があるので、オブジェクトを [in] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f688-111">The caller must supply a message for the API to fill out, so the object must go [in].</span></span> <span data-ttu-id="3f688-112">**Lpmessage**の種類の定義については、「mapidefs.h」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f688-112">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="3f688-113">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="3f688-113">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="3f688-114">順番この値は**null**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f688-114">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="3f688-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f688-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3f688-116">順番このパラメーターには、変換中に実行する特別なアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="3f688-116">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="3f688-117">特定のアクションを実行する必要がない場合、または次の値の組み合わせを指定する場合は、ゼロ (0) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f688-117">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="3f688-118">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3f688-118">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="3f688-119">送信/未送信の情報は、X 未送信の情報として保持されます。</span><span class="sxs-lookup"><span data-stu-id="3f688-119">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="3f688-120">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="3f688-120">CCSF_SMTP</span></span>
  
> <span data-ttu-id="3f688-121">MIME ストリームは、SMTP (Simple Mail Transfer Protocol) メッセージに対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f688-121">The MIME stream is for a Simple Mail Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="3f688-122">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="3f688-122">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="3f688-123">MIME ストリームの BCC 受信者は、MAPI メッセージに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f688-123">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="3f688-124">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="3f688-124">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="3f688-125">MIME ストリームの HTML 本文は、MAPI メッセージでリッチテキスト形式 (RTF) に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f688-125">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>

<span data-ttu-id="3f688-126">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3f688-126">CCSF_GLOBAL_MESSAGE</span></span>
> <span data-ttu-id="3f688-127">コンバータは、MIME ストリームを国際メッセージ (EAI/RFC6530) として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f688-127">The converter should handle the MIME stream as an international message (EAI/RFC6530).</span></span> <span data-ttu-id="3f688-128">Outlook 2013 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3f688-128">Not supported on Outlook 2013.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3f688-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="3f688-129">Return value</span></span>

<span data-ttu-id="3f688-130">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3f688-130">E_INVALIDARG</span></span>
  
> <span data-ttu-id="3f688-131">_Pstm_が**null**、 _Pmsg_が**null**、 _ulflags_が無効であることを示します。</span><span class="sxs-lookup"><span data-stu-id="3f688-131">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3f688-132">備考</span><span class="sxs-lookup"><span data-stu-id="3f688-132">Remarks</span></span>

<span data-ttu-id="3f688-133">_Ulflags_の一部として**CCSF_USE_RTF**を指定し、宛先のメッセージストアが html と rtf の両方をサポートしている場合、MAPI メッセージは html または rtf に変換されます。</span><span class="sxs-lookup"><span data-stu-id="3f688-133">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="3f688-134">メッセージが RTF に変換される場合、変換された形式は RTF 形式に変換され、すべての HTML が圧縮 RTF 文字列に埋め込まれ、文字列が[PidTagRtfCompressed 標準プロパティ](pidtagrtfcompressed-canonical-property.md)に格納されます。</span><span class="sxs-lookup"><span data-stu-id="3f688-134">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3f688-135">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="3f688-135">MFCMAPI reference</span></span>

<span data-ttu-id="3f688-136">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f688-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3f688-137">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="3f688-137">**File**</span></span>|<span data-ttu-id="3f688-138">**関数**</span><span class="sxs-lookup"><span data-stu-id="3f688-138">**Function**</span></span>|<span data-ttu-id="3f688-139">**コメント**</span><span class="sxs-lookup"><span data-stu-id="3f688-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f688-140">MapiMime .cpp</span><span class="sxs-lookup"><span data-stu-id="3f688-140">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3f688-141">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="3f688-141">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="3f688-142">MFCMAPI は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="3f688-142">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="3f688-143">MapiMime .cpp</span><span class="sxs-lookup"><span data-stu-id="3f688-143">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="3f688-144">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="3f688-144">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="3f688-145">MFCMAPI は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="3f688-145">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f688-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f688-146">See also</span></span>



[<span data-ttu-id="3f688-147">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f688-147">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="3f688-148">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="3f688-148">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="3f688-149">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="3f688-149">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="3f688-150">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="3f688-150">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="3f688-151">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="3f688-151">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="3f688-152">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="3f688-152">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="3f688-153">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="3f688-153">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="3f688-154">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="3f688-154">MAPI Constants</span></span>](mapi-constants.md)

