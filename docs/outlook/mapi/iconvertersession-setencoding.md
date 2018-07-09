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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a13d4e54900989c692add85add6853a1b511f448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800420"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="1ef96-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="1ef96-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="1ef96-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ef96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ef96-105">変換時に使用するエンコーディングを初期化します。</span><span class="sxs-lookup"><span data-stu-id="1ef96-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="1ef96-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1ef96-106">Parameters</span></span>

<span data-ttu-id="1ef96-107">_et_</span><span class="sxs-lookup"><span data-stu-id="1ef96-107">_et_</span></span>
  
> <span data-ttu-id="1ef96-108">( [ENCODINGTYPE](http://msdn.microsoft.com/ja-jp/library/aa374936%28VS.85%29.aspx) ) の値です。</span><span class="sxs-lookup"><span data-stu-id="1ef96-108">An [ENCODINGTYPE](http://msdn.microsoft.com/ja-jp/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="1ef96-109">次の値のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="1ef96-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="1ef96-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="1ef96-110">IET_BASE64</span></span>
   - <span data-ttu-id="1ef96-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="1ef96-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="1ef96-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="1ef96-112">IET_QP</span></span>
   - <span data-ttu-id="1ef96-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="1ef96-113">IET_7BIT</span></span>
   - <span data-ttu-id="1ef96-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="1ef96-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ef96-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1ef96-115">Return value</span></span>

<span data-ttu-id="1ef96-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1ef96-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="1ef96-117">渡されるエンコードの種類が無効でした。</span><span class="sxs-lookup"><span data-stu-id="1ef96-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ef96-118">備考</span><span class="sxs-lookup"><span data-stu-id="1ef96-118">Remarks</span></span>

<span data-ttu-id="1ef96-119">[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を使用して変換を実行する前に、 **SetEncoding**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1ef96-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="1ef96-120">メール アイテムの最も外側のメッセージの本文のみのエンコーディングを設定するのにには、 **SetEncoding**を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ef96-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="1ef96-121">Microsoft Outlook 2010 と Microsoft Outlook 2013 は、個々 の添付ファイルのエンコーディングを選択します。</span><span class="sxs-lookup"><span data-stu-id="1ef96-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ef96-122">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1ef96-122">MFCMAPI reference</span></span>

<span data-ttu-id="1ef96-123">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1ef96-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ef96-124">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1ef96-124">**File**</span></span>|<span data-ttu-id="1ef96-125">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1ef96-125">**Function**</span></span>|<span data-ttu-id="1ef96-126">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1ef96-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ef96-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="1ef96-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="1ef96-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="1ef96-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="1ef96-129">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="1ef96-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="1ef96-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="1ef96-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="1ef96-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="1ef96-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="1ef96-132">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="1ef96-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ef96-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ef96-133">See also</span></span>

- [<span data-ttu-id="1ef96-134">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ef96-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="1ef96-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="1ef96-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="1ef96-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="1ef96-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="1ef96-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="1ef96-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="1ef96-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="1ef96-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="1ef96-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="1ef96-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="1ef96-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="1ef96-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="1ef96-141">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="1ef96-141">MAPI Constants</span></span>](mapi-constants.md)

