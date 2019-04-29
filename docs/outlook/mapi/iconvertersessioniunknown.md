---
title: iconvertersession IUnknown
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432318"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="9615a-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9615a-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="9615a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9615a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9615a-105">MIME オブジェクトと MAPI メッセージ間の変換を可能にします。</span><span class="sxs-lookup"><span data-stu-id="9615a-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="9615a-106">これは、インターネット経由でメッセージを転送する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9615a-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9615a-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="9615a-107">Provided by:</span></span>  <br/> |<span data-ttu-id="9615a-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="9615a-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="9615a-109">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="9615a-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9615a-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="9615a-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9615a-111">v の順序</span><span class="sxs-lookup"><span data-stu-id="9615a-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9615a-112">**[setadrbook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="9615a-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="9615a-113">mapi メッセージを mime ストリームに変換するときに、あいまいなアドレスを解決するために mapi から mime コンバータが使用するオプションの mapi アドレス帳を指定します。</span><span class="sxs-lookup"><span data-stu-id="9615a-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="9615a-114">**[setencoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="9615a-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="9615a-115">変換時に使用するエンコードを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9615a-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="9615a-116">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="9615a-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9615a-117">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="9615a-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9615a-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="9615a-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="9615a-119">MIME ストリームを MAPI メッセージに変換します。</span><span class="sxs-lookup"><span data-stu-id="9615a-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="9615a-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="9615a-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="9615a-121">MAPI メッセージを MIME ストリームに変換します。</span><span class="sxs-lookup"><span data-stu-id="9615a-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="9615a-122">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="9615a-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9615a-123">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="9615a-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9615a-124">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="9615a-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9615a-125">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="9615a-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9615a-126">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="9615a-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9615a-127">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="9615a-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9615a-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="9615a-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="9615a-129">**MAPIToMIMEStm**でコンバータが返す MIME ストリームのテキストの折り返し幅を設定します。</span><span class="sxs-lookup"><span data-stu-id="9615a-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="9615a-130">**[setsaveformat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9615a-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="9615a-131">コンバーターが**MAPIToMIMEStm**で MIME ストリームを返す形式を設定します。</span><span class="sxs-lookup"><span data-stu-id="9615a-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="9615a-132">*Placeholder メンバー*</span><span class="sxs-lookup"><span data-stu-id="9615a-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9615a-133">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="9615a-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9615a-134">**[setcharset](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="9615a-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="9615a-135">mapi メッセージを mime ストリームに変換するときに mapi から mime コンバータが使用するオプションの文字セットを指定します。</span><span class="sxs-lookup"><span data-stu-id="9615a-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9615a-136">注釈</span><span class="sxs-lookup"><span data-stu-id="9615a-136">Remarks</span></span>

<span data-ttu-id="9615a-137">**MAPIToMIMEStm**を使用して変換を実行する前に、 **setencoding**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9615a-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9615a-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="9615a-138">See also</span></span>



[<span data-ttu-id="9615a-139">MAPI-MIME 会話 API について</span><span class="sxs-lookup"><span data-stu-id="9615a-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="9615a-140">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="9615a-140">MAPI Constants</span></span>](mapi-constants.md)

