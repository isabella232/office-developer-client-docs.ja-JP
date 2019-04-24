---
title: iconvertersessionsetsaveformat
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336639"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="1cc80-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="1cc80-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="1cc80-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cc80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cc80-105">[iconvertersession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md)で、コンバータが MIME ストリームを返す形式を設定します。</span><span class="sxs-lookup"><span data-stu-id="1cc80-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="1cc80-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1cc80-106">Parameters</span></span>

<span data-ttu-id="1cc80-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="1cc80-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="1cc80-108">順番MIME ストリームに使用される保存形式。</span><span class="sxs-lookup"><span data-stu-id="1cc80-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="1cc80-109">詳細については、「 [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx)」という列挙型を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc80-109">For more information, see the enum type [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="1cc80-110">**SAVE_RFC1521**: 既定の MIME を使用します。</span><span class="sxs-lookup"><span data-stu-id="1cc80-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="1cc80-111">**SAVE_RFC822**: uuencode を使用します。</span><span class="sxs-lookup"><span data-stu-id="1cc80-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1cc80-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="1cc80-112">Return values</span></span>

<span data-ttu-id="1cc80-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cc80-113">S_OK</span></span>
  
> <span data-ttu-id="1cc80-114">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="1cc80-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1cc80-115">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="1cc80-115">MFCMAPI reference</span></span>

<span data-ttu-id="1cc80-116">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1cc80-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1cc80-117">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="1cc80-117">**File**</span></span>|<span data-ttu-id="1cc80-118">**関数**</span><span class="sxs-lookup"><span data-stu-id="1cc80-118">**Function**</span></span>|<span data-ttu-id="1cc80-119">**コメント**</span><span class="sxs-lookup"><span data-stu-id="1cc80-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1cc80-120">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="1cc80-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="1cc80-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="1cc80-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="1cc80-122">mfcmapi は MimeToMAPI を使用して、EML ファイルを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="1cc80-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="1cc80-123">mapimime .cpp</span><span class="sxs-lookup"><span data-stu-id="1cc80-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="1cc80-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="1cc80-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="1cc80-125">mfcmapi は、MAPIToMIMEStm を使用して MAPI メッセージを EML ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="1cc80-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1cc80-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cc80-126">See also</span></span>

- [<span data-ttu-id="1cc80-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cc80-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="1cc80-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="1cc80-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="1cc80-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="1cc80-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="1cc80-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="1cc80-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="1cc80-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="1cc80-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="1cc80-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="1cc80-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="1cc80-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="1cc80-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="1cc80-134">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="1cc80-134">MAPI Constants</span></span>](mapi-constants.md)

