---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: '最終更新日: 2017 年 9 月 20日'
ms.openlocfilehash: b59114926d44ba613efbbde1c8dd5d17c26756c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800407"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="032b5-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="032b5-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="032b5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="032b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="032b5-105">MAPI メッセージを MIME ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="032b5-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="032b5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="032b5-106">Parameters</span></span>

 <span data-ttu-id="032b5-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="032b5-107">_pmsg_</span></span>
  
> <span data-ttu-id="032b5-108">[in]変換するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="032b5-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="032b5-109">**LPMESSAGE**の型定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="032b5-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="032b5-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="032b5-110">_pstm_</span></span>
  
> <span data-ttu-id="032b5-111">[out]ストリームを出力する[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="032b5-111">[out] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="032b5-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="032b5-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="032b5-113">[in]コンバーターで特定のアクションを示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="032b5-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="032b5-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="032b5-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="032b5-115">コンバーターは、8 ビットのヘッダーを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="032b5-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="032b5-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="032b5-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="032b5-117">未送信の X で送信された未送信の情報が保持されます。</span><span class="sxs-lookup"><span data-stu-id="032b5-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="032b5-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="032b5-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="032b5-119">コンバーターは、国際的なメッセージ (EAI/RFC6530) を構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="032b5-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="032b5-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="032b5-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="032b5-121">MAPI メッセージの BCC 受信者は、MIME ストリームに入れるべきです。</span><span class="sxs-lookup"><span data-stu-id="032b5-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="032b5-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="032b5-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="032b5-123">送信メッセージのメッセージ Id フィールドは含まれません。</span><span class="sxs-lookup"><span data-stu-id="032b5-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="032b5-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="032b5-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="032b5-125">コンバーターでは、外部のメッセージのヘッダーを無視してください。</span><span class="sxs-lookup"><span data-stu-id="032b5-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="032b5-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="032b5-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="032b5-127">コンバーター テキスト形式を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="032b5-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="032b5-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="032b5-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="032b5-129">コンバーターは、SMTP メッセージが渡されています。</span><span class="sxs-lookup"><span data-stu-id="032b5-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="032b5-130">このフラグを設定することが常にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="032b5-130">This flag must always be set.</span></span>
    
<span data-ttu-id="032b5-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="032b5-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="032b5-132">コンバーターは、HTML から MIME メッセージ内の RTF 形式に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="032b5-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="032b5-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="032b5-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="032b5-134">コンバーターでは、MIME メッセージのトランスポート ニュートラル カプセル化形式 (TNEF) 形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="032b5-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="032b5-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="032b5-135">Return values</span></span>

<span data-ttu-id="032b5-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="032b5-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="032b5-137">無効なフラグが渡された、または*pmsg*または*pstm*では NULL です。</span><span class="sxs-lookup"><span data-stu-id="032b5-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="032b5-138">備考</span><span class="sxs-lookup"><span data-stu-id="032b5-138">Remarks</span></span>

<span data-ttu-id="032b5-139">標準の Outlook メッセージの種類に対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="032b5-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="032b5-140">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="032b5-140">MFCMAPI reference</span></span>

<span data-ttu-id="032b5-141">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="032b5-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="032b5-142">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="032b5-142">**File**</span></span>|<span data-ttu-id="032b5-143">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="032b5-143">**Function**</span></span>|<span data-ttu-id="032b5-144">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="032b5-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="032b5-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="032b5-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="032b5-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="032b5-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="032b5-147">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="032b5-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="032b5-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="032b5-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="032b5-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="032b5-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="032b5-150">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="032b5-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="032b5-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="032b5-151">See also</span></span>



[<span data-ttu-id="032b5-152">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="032b5-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="032b5-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="032b5-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="032b5-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="032b5-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="032b5-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="032b5-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="032b5-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="032b5-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="032b5-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="032b5-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="032b5-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="032b5-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="032b5-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="032b5-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="032b5-160">PidTagMessageEditorFormat の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="032b5-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="032b5-161">PidLidUseTnef ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="032b5-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="032b5-162">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="032b5-162">MAPI Constants</span></span>](mapi-constants.md)

