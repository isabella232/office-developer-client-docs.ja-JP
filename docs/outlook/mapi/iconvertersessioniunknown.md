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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a89b1a93b2b03f97426a3988739e9b0d8411f113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800426"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="572ef-103">IConverterSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="572ef-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="572ef-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="572ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="572ef-105">MIME オブジェクト、および MAPI メッセージ間の変換を使用できます。</span><span class="sxs-lookup"><span data-stu-id="572ef-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="572ef-106">これは、インターネット経由でメッセージの転送に便利なことができます。</span><span class="sxs-lookup"><span data-stu-id="572ef-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="572ef-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="572ef-107">Provided by:</span></span>  <br/> |<span data-ttu-id="572ef-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="572ef-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="572ef-109">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="572ef-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="572ef-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="572ef-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="572ef-111">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="572ef-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="572ef-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="572ef-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="572ef-113">MAPI メッセージを MIME ストリームに変換するときにあいまいなアドレスを解決するのには MIME コンバーターに MAPI を使用して MAPI アドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="572ef-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="572ef-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="572ef-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="572ef-115">変換時に使用するエンコーディングを初期化します。</span><span class="sxs-lookup"><span data-stu-id="572ef-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="572ef-116">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="572ef-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="572ef-117">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="572ef-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="572ef-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="572ef-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="572ef-119">MIME ストリームを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="572ef-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="572ef-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="572ef-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="572ef-121">MAPI メッセージを MIME ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="572ef-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="572ef-122">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="572ef-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="572ef-123">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="572ef-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="572ef-124">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="572ef-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="572ef-125">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="572ef-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="572ef-126">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="572ef-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="572ef-127">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="572ef-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="572ef-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="572ef-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="572ef-129">テキストの折り返しの MIME ストリームを表すコンバーター **MAPIToMIMEStm**の幅を設定します。</span><span class="sxs-lookup"><span data-stu-id="572ef-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="572ef-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="572ef-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="572ef-131">コンバーターには、 **MAPIToMIMEStm**の MIME ストリームを取得する書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="572ef-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="572ef-132">*プレース ホルダー メンバー*</span><span class="sxs-lookup"><span data-stu-id="572ef-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="572ef-133">*いないサポートまたは文書化されています。*</span><span class="sxs-lookup"><span data-stu-id="572ef-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="572ef-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="572ef-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="572ef-135">MIME コンバーターに MAPI が MAPI メッセージを MIME ストリームに変換するときに使用する、省略可能な文字の設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="572ef-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="572ef-136">備考</span><span class="sxs-lookup"><span data-stu-id="572ef-136">Remarks</span></span>

<span data-ttu-id="572ef-137">**MAPIToMIMEStm**を使用して変換を実行する前に、 **SetEncoding**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="572ef-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="572ef-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="572ef-138">See also</span></span>



[<span data-ttu-id="572ef-139">MAPI から MIME 変換 API について</span><span class="sxs-lookup"><span data-stu-id="572ef-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="572ef-140">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="572ef-140">MAPI Constants</span></span>](mapi-constants.md)

