---
title: IConverterSessionSetCharSet
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
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 032f071e18af3a89a2850cf2bd1e141f34bc86d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800415"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="ec5ab-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="ec5ab-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="ec5ab-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec5ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec5ab-105">オプションの文字セットを MAPI MIME コンバーターの使用する MAPI メッセージを MIME ストリームに変換するときを指定します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="ec5ab-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ec5ab-106">Parameters</span></span>

 <span data-ttu-id="ec5ab-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="ec5ab-107">_fApply_</span></span>
  
> <span data-ttu-id="ec5ab-108">[in]特定の文字セット変換を使用するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="ec5ab-109">**真**以降の変換中の文字セットを適用するには、このパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="ec5ab-110">任意の特定の文字セットを適用し、後続のメッセージの既定値に戻す必要がなくなった場合は、 **false を指定**するこのパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="ec5ab-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="ec5ab-111">_hcharset_</span></span>
  
> <span data-ttu-id="ec5ab-112">[in]Windows メールの mimeole.h で定義されているように設定する文字へのハンドル。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="ec5ab-113">指定**null**を任意の特定の文字セットを適用しないことを指定します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="ec5ab-114">非**null**値は、文字セットへのハンドルを取得するのには[MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx)のような関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="ec5ab-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="ec5ab-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="ec5ab-116">[in]Windows メールの mimeole.h で定義されている、メッセージの変換を設定する文字を適用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec5ab-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ec5ab-117">Return value</span></span>

<span data-ttu-id="ec5ab-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec5ab-118">S_OK</span></span>
  
> <span data-ttu-id="ec5ab-119">関数の呼び出しが成功します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ec5ab-120">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ec5ab-120">MFCMAPI reference</span></span>

<span data-ttu-id="ec5ab-121">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ec5ab-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ec5ab-122">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ec5ab-122">**File**</span></span>|<span data-ttu-id="ec5ab-123">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ec5ab-123">**Function**</span></span>|<span data-ttu-id="ec5ab-124">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ec5ab-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec5ab-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ec5ab-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ec5ab-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="ec5ab-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="ec5ab-127">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="ec5ab-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ec5ab-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ec5ab-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="ec5ab-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="ec5ab-130">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="ec5ab-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec5ab-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec5ab-131">See also</span></span>



[<span data-ttu-id="ec5ab-132">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec5ab-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="ec5ab-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="ec5ab-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="ec5ab-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="ec5ab-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="ec5ab-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="ec5ab-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="ec5ab-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="ec5ab-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="ec5ab-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="ec5ab-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="ec5ab-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="ec5ab-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

