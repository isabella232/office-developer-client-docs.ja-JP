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
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336632"
---
# <a name="iconvertersessionsettextwrapping"></a><span data-ttu-id="e579e-103">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="e579e-103">IConverterSession::SetTextWrapping</span></span>

  
  
<span data-ttu-id="e579e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e579e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e579e-105">[iconvertersession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md)でコンバータが返す MIME ストリームのテキストの折り返し幅を設定します。</span><span class="sxs-lookup"><span data-stu-id="e579e-105">Sets the text wrapping width for a MIME stream that the converter will return in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a><span data-ttu-id="e579e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e579e-106">Parameters</span></span>

 <span data-ttu-id="e579e-107">*fWrapText*</span><span class="sxs-lookup"><span data-stu-id="e579e-107">*fWrapText*</span></span> 
  
> <span data-ttu-id="e579e-108">順番テキストを折り返すかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e579e-108">[in] Whether to wrap text or not.</span></span>
    
 <span data-ttu-id="e579e-109">*ulWrapWidth*</span><span class="sxs-lookup"><span data-stu-id="e579e-109">*ulWrapWidth*</span></span> 
  
> <span data-ttu-id="e579e-110">順番文字列の折り返し幅を使用します。</span><span class="sxs-lookup"><span data-stu-id="e579e-110">[in] The text wrapping width to use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e579e-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="e579e-111">Return value</span></span>

<span data-ttu-id="e579e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e579e-112">S_OK</span></span>
  
> <span data-ttu-id="e579e-113">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="e579e-113">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="e579e-114">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="e579e-114">MFCMAPI reference</span></span>

<span data-ttu-id="e579e-115">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e579e-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e579e-116">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="e579e-116">**File**</span></span>|<span data-ttu-id="e579e-117">**関数**</span><span class="sxs-lookup"><span data-stu-id="e579e-117">**Function**</span></span>|<span data-ttu-id="e579e-118">**コメント**</span><span class="sxs-lookup"><span data-stu-id="e579e-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e579e-119">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="e579e-119">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e579e-120">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="e579e-120">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="e579e-121">mfcmapi は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="e579e-121">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="e579e-122">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="e579e-122">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="e579e-123">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="e579e-123">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="e579e-124">mfcmapi は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="e579e-124">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e579e-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="e579e-125">See also</span></span>



[<span data-ttu-id="e579e-126">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e579e-126">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="e579e-127">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="e579e-127">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="e579e-128">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="e579e-128">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="e579e-129">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="e579e-129">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="e579e-130">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="e579e-130">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="e579e-131">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="e579e-131">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="e579e-132">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="e579e-132">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)


[<span data-ttu-id="e579e-133">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="e579e-133">MAPI Constants</span></span>](mapi-constants.md)

