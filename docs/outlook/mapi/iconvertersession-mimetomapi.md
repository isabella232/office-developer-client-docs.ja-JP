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
ms.openlocfilehash: 60a058cc119290a0e14a76c914ac6d5a2d7a693b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593019"
---
# <a name="iconvertersessionmimetomapi"></a><span data-ttu-id="ec52c-103">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="ec52c-103">IConverterSession::MIMEToMAPI</span></span>

  
  
<span data-ttu-id="ec52c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec52c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec52c-105">MIME ストリームを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="ec52c-105">Converts a MIME stream to a MAPI message.</span></span>
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="ec52c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ec52c-106">Parameters</span></span>

 <span data-ttu-id="ec52c-107">_pstm_</span><span class="sxs-lookup"><span data-stu-id="ec52c-107">_pstm_</span></span>
  
> <span data-ttu-id="ec52c-108">[in]MIME ストリームの[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="ec52c-108">[in] [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface to a MIME stream.</span></span> 
    
 <span data-ttu-id="ec52c-109">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="ec52c-109">_pmsg_</span></span>
  
> <span data-ttu-id="ec52c-110">[out]ロードするのには、メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ec52c-110">[out] Pointer to the message to load.</span></span> <span data-ttu-id="ec52c-111">**LPMESSAGE**の型定義の mapidefs.h を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec52c-111">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span>
    
 <span data-ttu-id="ec52c-112">_pszSrcSrv_</span><span class="sxs-lookup"><span data-stu-id="ec52c-112">_pszSrcSrv_</span></span>
  
> <span data-ttu-id="ec52c-113">[in]この値を**null**にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec52c-113">[in] This value must be **null**.</span></span>
    
 <span data-ttu-id="ec52c-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec52c-114">_ulFlags_</span></span>
  
> <span data-ttu-id="ec52c-115">[in]このパラメーターは、変換中に実行される特別な操作を識別します。</span><span class="sxs-lookup"><span data-stu-id="ec52c-115">[in] This parameter identifies any special action to be taken during the conversion.</span></span> <span data-ttu-id="ec52c-116">ゼロ (0) を実行するには、特定のアクションがない場合、または次の値の組み合わせである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec52c-116">It must be zero (0) if no specific action is to be taken, or a combination of the following values:</span></span>
    
<span data-ttu-id="ec52c-117">CCSF_EMBEDDED_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="ec52c-117">CCSF_EMBEDDED_MESSAGE</span></span>
  
> <span data-ttu-id="ec52c-118">未送信の X で送信された未送信の情報が保持されます。</span><span class="sxs-lookup"><span data-stu-id="ec52c-118">Sent/unsent information is persisted in X-Unsent.</span></span>
    
<span data-ttu-id="ec52c-119">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="ec52c-119">CCSF_SMTP</span></span>
  
> <span data-ttu-id="ec52c-120">MIME ストリームでは、簡易 MAPI 転送プロトコル (SMTP) メッセージです。</span><span class="sxs-lookup"><span data-stu-id="ec52c-120">The MIME stream is for a Simple MAPI Transfer Protocol (SMTP) message.</span></span>
    
<span data-ttu-id="ec52c-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="ec52c-121">CCSF_INCLUDE_BCC</span></span>
  
> <span data-ttu-id="ec52c-122">MIME ストリームの BCC 受信者が MAPI メッセージに含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec52c-122">BCC recipients of the MIME stream should be included in the MAPI message.</span></span>
    
<span data-ttu-id="ec52c-123">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="ec52c-123">CCSF_USE_RTF</span></span>
  
> <span data-ttu-id="ec52c-124">MAPI メッセージの MIME ストリームの HTML 本文をリッチ テキスト形式 (RTF) に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec52c-124">The HTML body of the MIME stream should be converted to Rich Text Format (RTF) in the MAPI message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec52c-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="ec52c-125">Return value</span></span>

<span data-ttu-id="ec52c-126">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ec52c-126">E_INVALIDARG</span></span>
  
> <span data-ttu-id="ec52c-127">_Pstm_が**null**こと、 _pmsg_が**null**、または、 _ulFlags_が有効ではありませんを示します。</span><span class="sxs-lookup"><span data-stu-id="ec52c-127">Indicates that  _pstm_ is **null**,  _pmsg_ is **null**, or  _ulFlags_ is invalid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ec52c-128">注釈</span><span class="sxs-lookup"><span data-stu-id="ec52c-128">Remarks</span></span>

<span data-ttu-id="ec52c-129">_UlFlags_の一部として**CCSF_USE_RTF**を指定した送信先メッセージ ・ ストアが HTML や rtf 形式の両方をサポートしている場合は、MAPI メッセージは、html 形式または rtf 形式に変換されます。</span><span class="sxs-lookup"><span data-stu-id="ec52c-129">If you have specified **CCSF_USE_RTF** as part of  _ulFlags_ and the destination message store supports both HTML and RTF, the MAPI message will be converted to either HTML or RTF.</span></span> <span data-ttu-id="ec52c-130">変換後のフォーマットを圧縮する場合は、メッセージを rtf 形式に変換すると、rtf 形式、HTML は、圧縮された RTF 文字列に埋め込まれ、 [PidTagRtfCompressed の標準的なプロパティ](pidtagrtfcompressed-canonical-property.md)に文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec52c-130">If the message is converted to RTF, the converted format will be compressed RTF, any HTML will be embedded in the compressed RTF string, and the string will be contained in the [PidTagRtfCompressed Canonical Property](pidtagrtfcompressed-canonical-property.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ec52c-131">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ec52c-131">MFCMAPI reference</span></span>

<span data-ttu-id="ec52c-132">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ec52c-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ec52c-133">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ec52c-133">**File**</span></span>|<span data-ttu-id="ec52c-134">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ec52c-134">**Function**</span></span>|<span data-ttu-id="ec52c-135">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ec52c-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec52c-136">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ec52c-136">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ec52c-137">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="ec52c-137">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="ec52c-138">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="ec52c-138">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="ec52c-139">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ec52c-139">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ec52c-140">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="ec52c-140">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="ec52c-141">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="ec52c-141">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec52c-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec52c-142">See also</span></span>



[<span data-ttu-id="ec52c-143">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec52c-143">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="ec52c-144">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="ec52c-144">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="ec52c-145">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="ec52c-145">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="ec52c-146">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="ec52c-146">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="ec52c-147">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="ec52c-147">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="ec52c-148">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="ec52c-148">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="ec52c-149">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="ec52c-149">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)


[<span data-ttu-id="ec52c-150">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="ec52c-150">MAPI Constants</span></span>](mapi-constants.md)

