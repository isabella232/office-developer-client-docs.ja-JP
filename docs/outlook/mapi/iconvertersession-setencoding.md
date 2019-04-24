---
title: iconvertersessionsetencoding
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341301"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="e2820-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="e2820-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="e2820-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2820-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2820-105">変換時に使用されるエンコードを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e2820-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="e2820-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2820-106">Parameters</span></span>

<span data-ttu-id="e2820-107">_et_</span><span class="sxs-lookup"><span data-stu-id="e2820-107">_et_</span></span>
  
> <span data-ttu-id="e2820-108">[ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx)値。</span><span class="sxs-lookup"><span data-stu-id="e2820-108">An [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="e2820-109">次の値のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e2820-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="e2820-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="e2820-110">IET_BASE64</span></span>
   - <span data-ttu-id="e2820-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="e2820-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="e2820-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="e2820-112">IET_QP</span></span>
   - <span data-ttu-id="e2820-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="e2820-113">IET_7BIT</span></span>
   - <span data-ttu-id="e2820-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="e2820-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2820-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="e2820-115">Return value</span></span>

<span data-ttu-id="e2820-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e2820-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="e2820-117">渡されたエンコードの種類が無効です。</span><span class="sxs-lookup"><span data-stu-id="e2820-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2820-118">解説</span><span class="sxs-lookup"><span data-stu-id="e2820-118">Remarks</span></span>

<span data-ttu-id="e2820-119">[iconvertersession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を使用して変換を実行する前に、 **setencoding**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e2820-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="e2820-120">**setencoding**を使用して、メールアイテムの最も外側のメッセージ本文にのみエンコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="e2820-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="e2820-121">microsoft outlook 2010 および microsoft outlook 2013 各添付ファイルのエンコード方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="e2820-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e2820-122">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="e2820-122">MFCMAPI reference</span></span>

<span data-ttu-id="e2820-123">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2820-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e2820-124">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="e2820-124">**File**</span></span>|<span data-ttu-id="e2820-125">**関数**</span><span class="sxs-lookup"><span data-stu-id="e2820-125">**Function**</span></span>|<span data-ttu-id="e2820-126">**コメント**</span><span class="sxs-lookup"><span data-stu-id="e2820-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2820-127">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="e2820-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e2820-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="e2820-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="e2820-129">mfcmapi は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="e2820-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="e2820-130">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="e2820-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e2820-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="e2820-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="e2820-132">mfcmapi は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="e2820-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2820-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2820-133">See also</span></span>

- [<span data-ttu-id="e2820-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2820-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="e2820-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="e2820-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="e2820-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="e2820-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="e2820-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="e2820-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="e2820-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="e2820-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="e2820-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="e2820-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="e2820-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="e2820-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="e2820-141">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="e2820-141">MAPI Constants</span></span>](mapi-constants.md)

