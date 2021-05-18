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
description: '最終更新日: 2017 年 9 月 20 日'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326945"
---
# <a name="iconvertersessionmapitomimestm"></a><span data-ttu-id="75184-103">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="75184-103">IConverterSession::MAPIToMIMEStm</span></span>
 
  
<span data-ttu-id="75184-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75184-105">MAPI メッセージを MIME ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="75184-105">Converts a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="75184-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="75184-106">Parameters</span></span>

 <span data-ttu-id="75184-107">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="75184-107">_pmsg_</span></span>
  
> <span data-ttu-id="75184-108">[in]変換するメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="75184-108">[in] Pointer to the message to convert.</span></span> <span data-ttu-id="75184-109">LPMESSAGE の型定義については、mapidefs.h **を参照してください**。</span><span class="sxs-lookup"><span data-stu-id="75184-109">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="75184-110">_pstm_</span><span class="sxs-lookup"><span data-stu-id="75184-110">_pstm_</span></span>
  
> <span data-ttu-id="75184-111">[out] [ストリームを](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 出力する IStream インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="75184-111">[out] [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface to output the stream.</span></span> 
    
 <span data-ttu-id="75184-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75184-112">_ulFlags_</span></span>
  
>  <span data-ttu-id="75184-113">[in]コンバーターの特定のアクションを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="75184-113">[in] Flags that indicate specific actions for the converter:</span></span> 
    
<span data-ttu-id="75184-114">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="75184-114">CCSF_8BITHEADERS</span></span>
  
> <span data-ttu-id="75184-115">コンバーターは 8 ビット ヘッダーを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75184-115">The converter should allow 8-bit headers.</span></span>
    
<span data-ttu-id="75184-116">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="75184-116">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="75184-117">送信/送信されていない情報は X-Unsent に保持されます。</span><span class="sxs-lookup"><span data-stu-id="75184-117">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="75184-118">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="75184-118">CCSF_GLOBAL_MESSAGE</span></span>
  
> <span data-ttu-id="75184-119">コンバーターは、国際メッセージ (EAI/RFC6530) を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75184-119">The converter should build an international message (EAI/RFC6530).</span></span>
    
<span data-ttu-id="75184-120">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="75184-120">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="75184-121">MAPI メッセージの BCC 受信者は MIME ストリームに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="75184-121">BCC recipients of the MAPI message should be included in the MIME stream.</span></span>
    
<span data-ttu-id="75184-122">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="75184-122">CCSF_NO_MSGID</span></span>
  
> <span data-ttu-id="75184-123">送信メッセージにMessage-Idフィールドを含めない。</span><span class="sxs-lookup"><span data-stu-id="75184-123">Do not include Message-Id field in outgoing messages.</span></span>
    
<span data-ttu-id="75184-124">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="75184-124">CCSF_NOHEADERS</span></span>
  
> <span data-ttu-id="75184-125">コンバーターは、外部メッセージのヘッダーを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75184-125">The converter should ignore the headers of the outside message.</span></span>
    
<span data-ttu-id="75184-126">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="75184-126">CCSF_PLAIN_TEXT_ONLY</span></span>
  
> <span data-ttu-id="75184-127">コンバーターはプレーン テキストを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75184-127">The converter should just send plain text.</span></span>
    
<span data-ttu-id="75184-128">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="75184-128">CCSF_SMTP</span></span>
  
> <span data-ttu-id="75184-129">コンバーターは SMTP メッセージを渡されています。</span><span class="sxs-lookup"><span data-stu-id="75184-129">The converter is being passed an SMTP message.</span></span> <span data-ttu-id="75184-130">このフラグは常に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75184-130">This flag must always be set.</span></span>
    
<span data-ttu-id="75184-131">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="75184-131">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="75184-132">コンバーターは、MIME メッセージで HTML から RTF 形式に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75184-132">The converter should convert from HTML to RTF format in the MIME message.</span></span>
    
<span data-ttu-id="75184-133">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="75184-133">CCSF_USE_TNEF</span></span>
  
> <span data-ttu-id="75184-134">コンバーターは、MIME メッセージでトランスポート ニュートラル カプセル化形式 (TNEF) 形式を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75184-134">The converter should use Transport Neutral Encapsulation Format (TNEF) format in the MIME message.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="75184-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="75184-135">Return values</span></span>

<span data-ttu-id="75184-136">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="75184-136">E_INVALIDARG</span></span>
  
> <span data-ttu-id="75184-137">無効なフラグが渡されたか  *、pmsg*  または  *pstm が*  NULL です。</span><span class="sxs-lookup"><span data-stu-id="75184-137">Invalid flags were passed, or  *pmsg*  or  *pstm*  is NULL.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="75184-138">注釈</span><span class="sxs-lookup"><span data-stu-id="75184-138">Remarks</span></span>

<span data-ttu-id="75184-139">標準の Outlook メッセージの種類でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="75184-139">Supported only for standard Outlook message types.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="75184-140">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="75184-140">MFCMAPI reference</span></span>

<span data-ttu-id="75184-141">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="75184-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="75184-142">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="75184-142">**File**</span></span>|<span data-ttu-id="75184-143">**関数**</span><span class="sxs-lookup"><span data-stu-id="75184-143">**Function**</span></span>|<span data-ttu-id="75184-144">**コメント**</span><span class="sxs-lookup"><span data-stu-id="75184-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="75184-145">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="75184-145">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="75184-146">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="75184-146">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="75184-147">MFCMAPI は MimeToMAPI を使用して EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="75184-147">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="75184-148">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="75184-148">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="75184-149">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="75184-149">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="75184-150">MFCMAPI は MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="75184-150">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75184-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="75184-151">See also</span></span>



[<span data-ttu-id="75184-152">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75184-152">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="75184-153">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="75184-153">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="75184-154">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="75184-154">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="75184-155">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="75184-155">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="75184-156">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="75184-156">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="75184-157">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="75184-157">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="75184-158">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="75184-158">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="75184-159">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="75184-159">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
  
[<span data-ttu-id="75184-160">PidTagMessageEditorFormat 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="75184-160">PidTagMessageEditorFormat Canonical Property</span></span>](pidtagmessageeditorformat-canonical-property.md)
  
[<span data-ttu-id="75184-161">PidLidUseTnef ���K���̃v���p�e�B</span><span class="sxs-lookup"><span data-stu-id="75184-161">PidLidUseTnef Canonical Property</span></span>](pidlidusetnef-canonical-property.md)


[<span data-ttu-id="75184-162">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="75184-162">MAPI Constants</span></span>](mapi-constants.md)

