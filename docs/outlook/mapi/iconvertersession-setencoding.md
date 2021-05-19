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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341301"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="fc3e5-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="fc3e5-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="fc3e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc3e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc3e5-105">変換時に使用するエンコードを初期化します。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="fc3e5-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fc3e5-106">Parameters</span></span>

<span data-ttu-id="fc3e5-107">_et_</span><span class="sxs-lookup"><span data-stu-id="fc3e5-107">_et_</span></span>
  
> <span data-ttu-id="fc3e5-108">[ENCODINGTYPE 値](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-108">An [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="fc3e5-109">次の値だけがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="fc3e5-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="fc3e5-110">IET_BASE64</span></span>
   - <span data-ttu-id="fc3e5-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="fc3e5-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="fc3e5-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="fc3e5-112">IET_QP</span></span>
   - <span data-ttu-id="fc3e5-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="fc3e5-113">IET_7BIT</span></span>
   - <span data-ttu-id="fc3e5-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="fc3e5-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fc3e5-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="fc3e5-115">Return value</span></span>

<span data-ttu-id="fc3e5-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fc3e5-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="fc3e5-117">渡されたエンコードの種類が無効でした。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc3e5-118">注釈</span><span class="sxs-lookup"><span data-stu-id="fc3e5-118">Remarks</span></span>

<span data-ttu-id="fc3e5-119">[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を使用して変換を実行する前に **、SetEncoding** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="fc3e5-120">**SetEncoding を使用** して、メール アイテムの最も外側のメッセージ本文のエンコードのみを設定します。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="fc3e5-121">Microsoft Outlook 2010 Microsoft Outlook 2013 では、個々の添付ファイルのエンコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fc3e5-122">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="fc3e5-122">MFCMAPI reference</span></span>

<span data-ttu-id="fc3e5-123">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fc3e5-124">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="fc3e5-124">**File**</span></span>|<span data-ttu-id="fc3e5-125">**関数**</span><span class="sxs-lookup"><span data-stu-id="fc3e5-125">**Function**</span></span>|<span data-ttu-id="fc3e5-126">**コメント**</span><span class="sxs-lookup"><span data-stu-id="fc3e5-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc3e5-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="fc3e5-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="fc3e5-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="fc3e5-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="fc3e5-129">MFCMAPI は MimeToMAPI を使用して EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="fc3e5-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="fc3e5-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="fc3e5-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="fc3e5-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="fc3e5-132">MFCMAPI は MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="fc3e5-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc3e5-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc3e5-133">See also</span></span>

- [<span data-ttu-id="fc3e5-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fc3e5-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="fc3e5-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="fc3e5-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="fc3e5-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="fc3e5-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="fc3e5-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="fc3e5-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="fc3e5-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="fc3e5-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="fc3e5-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="fc3e5-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="fc3e5-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="fc3e5-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="fc3e5-141">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="fc3e5-141">MAPI Constants</span></span>](mapi-constants.md)

