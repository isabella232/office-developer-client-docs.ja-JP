---
title: メッセージ テキストを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 38be3bc2df8931ca45da12e43436377545e8a977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799888"
---
# <a name="creating-message-text"></a><span data-ttu-id="d22d3-103">メッセージ テキストを作成します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-103">Creating message text</span></span>

<span data-ttu-id="d22d3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d22d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d22d3-105">いくつかのメッセージは、受信者一覧と件名の行では、IPM では具体的には、ほとんどのメッセージの内容よりもそれ以上の構成されています。メッセージに注意してください、テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d22d3-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="d22d3-106">メッセージをテキスト形式または書式設定された、3 つのプロパティに格納されます: **PR\_本体**([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="d22d3-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="d22d3-107">設定の場合は、クライアントでは、テキスト ベースで**PR\_本文**。</span><span class="sxs-lookup"><span data-stu-id="d22d3-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="d22d3-108">**PR_RTF_COMPRESSED**のみまたは両方の**PR_RTF_COMPRESSED**のいずれかに設定で、リッチ テキスト形式式 (RTF) 書式設定されたテキストをサポートする場合、 **PR\_本文**に使用しているメッセージ ストア プロバイダーに依存します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="d22d3-109">RTF に対応して、クライアントは、rtf 形式に対応したメッセージ ・ ストアを使用しているときのみ**PR_RTF_COMPRESSED**を設定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="d22d3-110">RTF に対応して、クライアントが RTF に対応していないメッセージ ストアを使用している場合は、両方のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="d22d3-111">クライアントは、HTML をサポートする場合は、 **PR_HTML**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="d22d3-112">メッセージ ・ ストアがリッチ テキスト形式をサポートしているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="d22d3-113">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティを取得するために、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="d22d3-114">STORE_RTF_OK ビットを確認します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="d22d3-115">STORE_RTF_OK が設定されている場合、メッセージ ストア プロバイダーは、rtf 形式のテキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d22d3-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="d22d3-116">設定されていない場合、メッセージ ストア プロバイダーは、テキスト形式のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d22d3-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="d22d3-117">メッセージ ・ ストアが HTML をサポートしているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="d22d3-118">**PR_STORE_SUPPORT_MASK**プロパティを取得するために、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="d22d3-119">STORE_HTML_OK ビットを確認します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="d22d3-120">STORE_HTML_OK が設定されている場合、メッセージ ストア プロバイダーは、HTML テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d22d3-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-prrtfcompressed"></a><span data-ttu-id="d22d3-121">PR の設定\_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="d22d3-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="d22d3-122">**PR_RTF_COMPRESSED**プロパティを開くには、メッセージの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して、インターフェイス識別子として IID_IStream を指定して、タグを設定するフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="d22d3-123">STORE_UNCOMPRESSED_RTF ビットがメッセージ ストアの**PR_STORE_SUPPORT_MASK**プロパティで設定されている場合、STORE_UNCOMPRESSED_RTF フラグを渡す、 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="d22d3-124">呼び出すことによって、元のストリームを解放する、* * が * * メソッドです。</span><span class="sxs-lookup"><span data-stu-id="d22d3-124">Release the original stream by calling its ** IUnknown::Release ** method.</span></span> 
    
4. <span data-ttu-id="d22d3-125">いずれかを呼び出す * * IStream::Write * * または**WrapCompressedRTFStream**からメッセージのテキストをストリームに書き込むには、 **IStream::CopyTo**が返されます。</span><span class="sxs-lookup"><span data-stu-id="d22d3-125">Call either ** IStream::Write ** or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="d22d3-126">**コミット**し、**リリース**のメソッドを呼び出す、 **OpenProperty**メソッドから返されるストリーム。</span><span class="sxs-lookup"><span data-stu-id="d22d3-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="d22d3-127">この時点で、メッセージ ストア プロバイダーは、rtf 形式をサポートする場合に必要なすべてが行われます。</span><span class="sxs-lookup"><span data-stu-id="d22d3-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="d22d3-128">メッセージ ストア プロバイダーを作成してメッセージの内容を同期して、書式設定を処理するために依存することができます、 **PR\_本文**プロパティが必要な場合です。</span><span class="sxs-lookup"><span data-stu-id="d22d3-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="d22d3-129">RTF に対応してメッセージ ・ ストアでは、同期を処理するために[行う](rtfsync.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="d22d3-130">場合 RTF\_SYNC_BODY_CHANGED フラグが TRUE に設定されて、プロバイダーが**PR_BODY**プロパティを再計算します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="d22d3-131">メッセージ ストア プロバイダーが RTF をサポートしていない場合は、 **PR_BODY**プロパティを設定することで rtf 形式以外のメッセージの内容を追加することもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d22d3-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-prhtml"></a><span data-ttu-id="d22d3-132">PR_HTML を設定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="d22d3-133">**IStream**インターフェイスを使用して**PR_HTML**プロパティを表示する[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="d22d3-134">**OpenProperty**から返されるストリームにメッセージのテキスト データを書き込むには、 **IStream::Write**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="d22d3-135">変更をコミットし、そのメモリを解放するには、 **IStream::Commit**と**リ ス**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-prbody"></a><span data-ttu-id="d22d3-136">PR_BODY を設定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="d22d3-137">**IStream**インターフェイスを使用して**PR_BODY**プロパティを表示する[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="d22d3-138">**OpenProperty**から返されるストリームにメッセージのテキスト データを書き込むには、 **IStream::Write**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="d22d3-139">書式設定されたテキストの同期を[行う](rtfsync.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="d22d3-140">これは新しいメッセージであるため、rtf 形式とテキスト形式の両方のバージョンのメッセージ テキストが変更されたことを示すために RTF_SYNC_RTF_CHANGED と RTF_SYNC_BODY_CHANGED の両方のフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="d22d3-141">**** **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) など、メッセージ ストア プロバイダーを必要とするいくつかの関連するプロパティを設定し、それらをメッセージに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="d22d3-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="d22d3-142">変更をコミットし、そのメモリを解放するには、 **IStream::Commit**と**リ ス**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d22d3-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

