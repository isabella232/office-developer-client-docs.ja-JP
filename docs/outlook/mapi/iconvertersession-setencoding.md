---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3edcb422eb0e3dd415d49c5e014c8b69095e7ec1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577206"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="70f98-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="70f98-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="70f98-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70f98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70f98-105">変換時に使用するエンコーディングを初期化します。</span><span class="sxs-lookup"><span data-stu-id="70f98-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="70f98-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="70f98-106">Parameters</span></span>

<span data-ttu-id="70f98-107">_et_</span><span class="sxs-lookup"><span data-stu-id="70f98-107">_et_</span></span>
  
> <span data-ttu-id="70f98-108">( [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) ) の値です。</span><span class="sxs-lookup"><span data-stu-id="70f98-108">An [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="70f98-109">次の値のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="70f98-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="70f98-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="70f98-110">IET_BASE64</span></span>
   - <span data-ttu-id="70f98-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="70f98-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="70f98-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="70f98-112">IET_QP</span></span>
   - <span data-ttu-id="70f98-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="70f98-113">IET_7BIT</span></span>
   - <span data-ttu-id="70f98-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="70f98-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="70f98-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="70f98-115">Return value</span></span>

<span data-ttu-id="70f98-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="70f98-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="70f98-117">渡されるエンコードの種類が無効でした。</span><span class="sxs-lookup"><span data-stu-id="70f98-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70f98-118">注釈</span><span class="sxs-lookup"><span data-stu-id="70f98-118">Remarks</span></span>

<span data-ttu-id="70f98-119">[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を使用して変換を実行する前に、 **SetEncoding**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="70f98-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="70f98-120">メール アイテムの最も外側のメッセージの本文のみのエンコーディングを設定するのにには、 **SetEncoding**を使用します。</span><span class="sxs-lookup"><span data-stu-id="70f98-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="70f98-121">Microsoft Outlook 2010 と Microsoft Outlook 2013 は、個々 の添付ファイルのエンコーディングを選択します。</span><span class="sxs-lookup"><span data-stu-id="70f98-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="70f98-122">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="70f98-122">MFCMAPI reference</span></span>

<span data-ttu-id="70f98-123">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="70f98-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="70f98-124">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="70f98-124">**File**</span></span>|<span data-ttu-id="70f98-125">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="70f98-125">**Function**</span></span>|<span data-ttu-id="70f98-126">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="70f98-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="70f98-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="70f98-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="70f98-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="70f98-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="70f98-129">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="70f98-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="70f98-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="70f98-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="70f98-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="70f98-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="70f98-132">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="70f98-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70f98-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="70f98-133">See also</span></span>

- [<span data-ttu-id="70f98-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="70f98-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="70f98-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="70f98-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="70f98-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="70f98-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="70f98-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="70f98-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="70f98-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="70f98-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="70f98-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="70f98-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="70f98-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="70f98-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="70f98-141">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="70f98-141">MAPI Constants</span></span>](mapi-constants.md)

