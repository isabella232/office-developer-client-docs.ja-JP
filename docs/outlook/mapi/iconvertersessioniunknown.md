---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a89b1a93b2b03f97426a3988739e9b0d8411f113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800426"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="9f74a-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f74a-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="9f74a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9f74a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9f74a-105">MIME オブジェクト、および MAPI メッセージ間の変換を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9f74a-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="9f74a-106">これは、インターネット経由でメッセージの転送に便利なことができます。</span><span class="sxs-lookup"><span data-stu-id="9f74a-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f74a-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="9f74a-107">Provided by:</span></span>  <br/> |<span data-ttu-id="9f74a-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="9f74a-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="9f74a-109">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="9f74a-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9f74a-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="9f74a-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9f74a-111">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="9f74a-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9f74a-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="9f74a-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="9f74a-113">MAPI メッセージを MIME ストリームに変換するときにあいまいなアドレスを解決するのには MIME コンバーターに MAPI を使用して MAPI アドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f74a-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="9f74a-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="9f74a-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="9f74a-115">変換時に使用するエンコーディングを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9f74a-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="9f74a-116">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="9f74a-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9f74a-117">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="9f74a-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9f74a-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="9f74a-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="9f74a-119">MIME ストリームを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="9f74a-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="9f74a-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="9f74a-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="9f74a-121">MAPI メッセージを MIME ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="9f74a-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="9f74a-122">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="9f74a-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9f74a-123">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="9f74a-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9f74a-124">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="9f74a-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9f74a-125">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="9f74a-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9f74a-126">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="9f74a-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9f74a-127">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="9f74a-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9f74a-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="9f74a-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="9f74a-129">テキストの折り返しの MIME ストリームを表すコンバーター **MAPIToMIMEStm**の幅を設定します。</span><span class="sxs-lookup"><span data-stu-id="9f74a-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="9f74a-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9f74a-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="9f74a-131">コンバーターには、 **MAPIToMIMEStm**の MIME ストリームを取得する書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="9f74a-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="9f74a-132">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="9f74a-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9f74a-133">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="9f74a-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9f74a-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="9f74a-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="9f74a-135">MIME コンバーターに MAPI が MAPI メッセージを MIME ストリームに変換するときに使用する、省略可能な文字の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f74a-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f74a-136">注釈</span><span class="sxs-lookup"><span data-stu-id="9f74a-136">Remarks</span></span>

<span data-ttu-id="9f74a-137">**MAPIToMIMEStm**を使用して変換を実行する前に、 **SetEncoding**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9f74a-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f74a-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="9f74a-138">See also</span></span>



[<span data-ttu-id="9f74a-139">MAPI-MIME 会話 API について</span><span class="sxs-lookup"><span data-stu-id="9f74a-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="9f74a-140">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="9f74a-140">MAPI Constants</span></span>](mapi-constants.md)

