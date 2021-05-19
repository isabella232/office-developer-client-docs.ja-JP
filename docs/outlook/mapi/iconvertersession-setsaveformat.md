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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336639"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="ba79a-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="ba79a-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="ba79a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba79a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba79a-105">コンバーターが [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)で MIME ストリームを返す形式を設定します。</span><span class="sxs-lookup"><span data-stu-id="ba79a-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="ba79a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ba79a-106">Parameters</span></span>

<span data-ttu-id="ba79a-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="ba79a-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="ba79a-108">[in]MIME ストリームに使用する保存形式。</span><span class="sxs-lookup"><span data-stu-id="ba79a-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="ba79a-109">詳細については、列挙型 [MIMESAVETYPE を参照してください](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ba79a-109">For more information, see the enum type [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="ba79a-110">**SAVE_RFC1521**: 既定の MIME を使用します。</span><span class="sxs-lookup"><span data-stu-id="ba79a-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="ba79a-111">**SAVE_RFC822**: uuencode を使用します。</span><span class="sxs-lookup"><span data-stu-id="ba79a-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ba79a-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="ba79a-112">Return values</span></span>

<span data-ttu-id="ba79a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba79a-113">S_OK</span></span>
  
> <span data-ttu-id="ba79a-114">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="ba79a-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba79a-115">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ba79a-115">MFCMAPI reference</span></span>

<span data-ttu-id="ba79a-116">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ba79a-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba79a-117">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ba79a-117">**File**</span></span>|<span data-ttu-id="ba79a-118">**関数**</span><span class="sxs-lookup"><span data-stu-id="ba79a-118">**Function**</span></span>|<span data-ttu-id="ba79a-119">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ba79a-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba79a-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ba79a-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ba79a-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="ba79a-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="ba79a-122">MFCMAPI は MimeToMAPI を使用して EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="ba79a-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="ba79a-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="ba79a-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="ba79a-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="ba79a-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="ba79a-125">MFCMAPI は MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="ba79a-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba79a-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ba79a-126">See also</span></span>

- [<span data-ttu-id="ba79a-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba79a-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="ba79a-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="ba79a-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="ba79a-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="ba79a-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="ba79a-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="ba79a-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="ba79a-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="ba79a-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="ba79a-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="ba79a-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="ba79a-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="ba79a-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="ba79a-134">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="ba79a-134">MAPI Constants</span></span>](mapi-constants.md)

