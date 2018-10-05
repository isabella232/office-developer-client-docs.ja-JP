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
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382422"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="c4555-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="c4555-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="c4555-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4555-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4555-105">変換時に使用するエンコーディングを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c4555-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="c4555-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4555-106">Parameters</span></span>

<span data-ttu-id="c4555-107">_et_</span><span class="sxs-lookup"><span data-stu-id="c4555-107">_et_</span></span>
  
> <span data-ttu-id="c4555-108">( [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) ) の値です。</span><span class="sxs-lookup"><span data-stu-id="c4555-108">An [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="c4555-109">次の値のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="c4555-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="c4555-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="c4555-110">IET_BASE64</span></span>
   - <span data-ttu-id="c4555-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="c4555-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="c4555-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="c4555-112">IET_QP</span></span>
   - <span data-ttu-id="c4555-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="c4555-113">IET_7BIT</span></span>
   - <span data-ttu-id="c4555-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="c4555-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4555-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="c4555-115">Return value</span></span>

<span data-ttu-id="c4555-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c4555-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="c4555-117">渡されるエンコードの種類が無効でした。</span><span class="sxs-lookup"><span data-stu-id="c4555-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4555-118">備考</span><span class="sxs-lookup"><span data-stu-id="c4555-118">Remarks</span></span>

<span data-ttu-id="c4555-119">[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を使用して変換を実行する前に、 **SetEncoding**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c4555-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="c4555-120">メール アイテムの最も外側のメッセージの本文のみのエンコーディングを設定するのにには、 **SetEncoding**を使用します。</span><span class="sxs-lookup"><span data-stu-id="c4555-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="c4555-121">Microsoft Outlook 2010 と Microsoft Outlook 2013 は、個々 の添付ファイルのエンコーディングを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4555-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c4555-122">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c4555-122">MFCMAPI reference</span></span>

<span data-ttu-id="c4555-123">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4555-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c4555-124">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c4555-124">**File**</span></span>|<span data-ttu-id="c4555-125">**関数**</span><span class="sxs-lookup"><span data-stu-id="c4555-125">**Function**</span></span>|<span data-ttu-id="c4555-126">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c4555-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c4555-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="c4555-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="c4555-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="c4555-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="c4555-129">MFCMAPI では、MimeToMAPI を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="c4555-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="c4555-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="c4555-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="c4555-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="c4555-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="c4555-132">MFCMAPI では、MAPIToMIMEStm を使用して、MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="c4555-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4555-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4555-133">See also</span></span>

- [<span data-ttu-id="c4555-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4555-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="c4555-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="c4555-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="c4555-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="c4555-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="c4555-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="c4555-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="c4555-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="c4555-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="c4555-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="c4555-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="c4555-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="c4555-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="c4555-141">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="c4555-141">MAPI Constants</span></span>](mapi-constants.md)

