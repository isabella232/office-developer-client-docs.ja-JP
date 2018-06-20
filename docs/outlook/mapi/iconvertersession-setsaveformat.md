---
title: IConverterSessionSetSaveFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f1a4834fc600cc93eeb7fc96563723326c7f2169
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800422"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="9c6bf-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="9c6bf-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="9c6bf-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c6bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c6bf-105">コンバーターが[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)で、MIME ストリームを取得する書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="9c6bf-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="9c6bf-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9c6bf-106">Parameters</span></span>

<span data-ttu-id="9c6bf-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="9c6bf-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="9c6bf-108">[in]保存の MIME ストリームに使用する書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="9c6bf-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="9c6bf-109">詳細については、 [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx)列挙型を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c6bf-109">For more information, see the enum type [MIMESAVETYPE](http://msdn.microsoft.com/en-us/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="9c6bf-110">**SAVE_RFC1521**: 既定値は、MIME を使用します。</span><span class="sxs-lookup"><span data-stu-id="9c6bf-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="9c6bf-111">**SAVE_RFC822**: でも、uuencode を使用します。</span><span class="sxs-lookup"><span data-stu-id="9c6bf-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9c6bf-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="9c6bf-112">Return values</span></span>

<span data-ttu-id="9c6bf-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c6bf-113">S_OK</span></span>
  
> <span data-ttu-id="9c6bf-114">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="9c6bf-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9c6bf-115">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="9c6bf-115">MFCMAPI reference</span></span>

<span data-ttu-id="9c6bf-116">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="9c6bf-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9c6bf-117">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="9c6bf-117">**File**</span></span>|<span data-ttu-id="9c6bf-118">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="9c6bf-118">**Function**</span></span>|<span data-ttu-id="9c6bf-119">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="9c6bf-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9c6bf-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="9c6bf-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="9c6bf-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="9c6bf-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="9c6bf-122">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="9c6bf-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="9c6bf-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="9c6bf-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="9c6bf-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="9c6bf-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="9c6bf-125">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="9c6bf-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c6bf-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c6bf-126">See also</span></span>

- [<span data-ttu-id="9c6bf-127">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c6bf-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="9c6bf-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="9c6bf-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="9c6bf-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="9c6bf-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="9c6bf-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="9c6bf-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="9c6bf-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="9c6bf-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="9c6bf-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="9c6bf-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="9c6bf-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="9c6bf-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="9c6bf-134">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="9c6bf-134">MAPI Constants</span></span>](mapi-constants.md)

