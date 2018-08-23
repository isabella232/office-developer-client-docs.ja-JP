---
title: IConverterSessionSetTextWrapping
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 81771a263a7496042d4950b465c0d5b03290399b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800418"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="955df-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="955df-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="955df-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="955df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="955df-105">テキストの折り返しのコンバーターから[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)で返される MIME ストリームの幅を設定します。</span><span class="sxs-lookup"><span data-stu-id="955df-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="955df-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="955df-106">Parameters</span></span>

 <span data-ttu-id="955df-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="955df-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="955df-108">[in]テキストを折り返すかどうかどうか。</span><span class="sxs-lookup"><span data-stu-id="955df-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="955df-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="955df-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="955df-110">[in]テキストの折り返しの幅を使用します。</span><span class="sxs-lookup"><span data-stu-id="955df-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="955df-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="955df-111">Return value</span></span>

<span data-ttu-id="955df-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="955df-112">S_OK</span></span>
  
> <span data-ttu-id="955df-113">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="955df-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="955df-114">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="955df-114">MFCMAPI reference</span></span>

<span data-ttu-id="955df-115">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="955df-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="955df-116">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="955df-116">**File**</span></span>|<span data-ttu-id="955df-117">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="955df-117">**Function**</span></span>|<span data-ttu-id="955df-118">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="955df-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="955df-119">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="955df-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="955df-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="955df-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="955df-121">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="955df-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="955df-122">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="955df-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="955df-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="955df-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="955df-124">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="955df-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="955df-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="955df-125">See also</span></span>



[<span data-ttu-id="955df-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="955df-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="955df-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="955df-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="955df-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="955df-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="955df-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="955df-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="955df-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="955df-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="955df-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="955df-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="955df-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="955df-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="955df-133">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="955df-133">MAPI Constants</span></span>](mapi-constants.md)

