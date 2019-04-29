---
title: メッセージ テキストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428005"
---
# <a name="creating-message-text"></a><span data-ttu-id="0d8f4-103">メッセージ テキストの作成</span><span class="sxs-lookup"><span data-stu-id="0d8f4-103">Creating message text</span></span>

<span data-ttu-id="0d8f4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d8f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d8f4-105">一部のメッセージは、受信者リストと件名行 (特に、ほとんどのメッセージの内容) だけで構成されていますが、特に IPM.メモメッセージには、テキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="0d8f4-106">メッセージテキストは、標準または書式設定することができ、 **pr\_本文**([PidTagBody](pidtagbody-canonical-property.md))、 **pr\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、および**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) の3つのプロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="0d8f4-107">クライアントがプレーンテキストベースの場合は、 **PR\_本文**を設定します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="0d8f4-108">リッチテキスト形式 (RTF) で書式設定されたテキストをサポートする場合は、使用しているメッセージストアプロバイダーに応じて、 **PR_RTF_COMPRESSED** only または**PR_RTF_COMPRESSED**と**PR\_本文**のどちらかを設定します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="0d8f4-109">rtf 対応のクライアントが rtf 対応のメッセージストアを使用している場合、 **PR_RTF_COMPRESSED**のみが設定されます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="0d8f4-110">rtf 対応のクライアントが rtf 対応ではないメッセージストアを使用している場合、両方のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="0d8f4-111">クライアントが HTML をサポートしている場合は、 **PR_HTML**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="0d8f4-112">メッセージストアがリッチテキスト形式をサポートしているかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="0d8f4-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="0d8f4-113">メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="0d8f4-114">STORE_RTF_OK ビットをチェックします。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="0d8f4-115">STORE_RTF_OK が設定されている場合、メッセージストアプロバイダーは RTF テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="0d8f4-116">設定されていない場合、メッセージストアプロバイダーはプレーンテキストのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="0d8f4-117">メッセージストアが HTML をサポートしているかどうかを判断する</span><span class="sxs-lookup"><span data-stu-id="0d8f4-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="0d8f4-118">メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_STORE_SUPPORT_MASK**プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="0d8f4-119">STORE_HTML_OK ビットをチェックします。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="0d8f4-120">STORE_HTML_OK が設定されている場合、メッセージストアプロバイダーは HTML テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-prrtfcompressed"></a><span data-ttu-id="0d8f4-121">PR\_RTF_COMPRESSED の設定</span><span class="sxs-lookup"><span data-stu-id="0d8f4-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="0d8f4-122">メッセージの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_RTF_COMPRESSED**プロパティを開き、IID_IStream をインターフェイス識別子として指定し、MAPI_CREATE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="0d8f4-123">[WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出し、STORE_UNCOMPRESSED_RTF ビットがメッセージストアの**PR_STORE_SUPPORT_MASK**プロパティで設定されている場合は STORE_UNCOMPRESSED_RTF フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="0d8f4-124">\* \* IUnknown:: Release \* \* メソッドを呼び出して、元のストリームを解放します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-124">Release the original stream by calling its \*\* IUnknown::Release \*\* method.</span></span> 
    
4. <span data-ttu-id="0d8f4-125">\* \* IStream:: Write \* \* または**IStream:: CopyTo**を呼び出して、 **WrapCompressedRTFStream**から返されたストリームにメッセージテキストを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="0d8f4-126">**openproperty**メソッドから返されたストリームで、 **Commit**メソッドと**Release**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="0d8f4-127">この時点で、メッセージストアプロバイダーが RTF をサポートしている場合は、必要なすべての処理が完了しています。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="0d8f4-128">メッセージストアプロバイダーによって、メッセージの内容と書式設定の同期を処理したり、必要に応じて**PR\_本文**のプロパティを作成したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="0d8f4-129">RTF 対応のメッセージは、同期を処理するために、 [rtfsync](rtfsync.md)という呼び出しを格納します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="0d8f4-130">RTF\_SYNC_BODY_CHANGED フラグが TRUE に設定されている場合、プロバイダーは**PR_BODY**プロパティを再計算します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="0d8f4-131">メッセージストアプロバイダーが rtf をサポートしていない場合は、 **PR_BODY**プロパティを設定することによって、rtf 以外のメッセージコンテンツも追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-prhtml"></a><span data-ttu-id="0d8f4-132">PR_HTML の設定</span><span class="sxs-lookup"><span data-stu-id="0d8f4-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="0d8f4-133">[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IStream**インターフェイスを使用して**PR_HTML**プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="0d8f4-134">呼び出し**IStream:: write**は、 **openproperty**から返されたストリームにメッセージテキストデータを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="0d8f4-135">変更をコミットしてメモリを解放するため、 **IStream:: commit**および**IUnknown:: Release**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-prbody"></a><span data-ttu-id="0d8f4-136">PR_BODY の設定</span><span class="sxs-lookup"><span data-stu-id="0d8f4-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="0d8f4-137">[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IStream**インターフェイスを使用して**PR_BODY**プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="0d8f4-138">呼び出し**IStream:: write**は、 **openproperty**から返されたストリームにメッセージテキストデータを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="0d8f4-139">[rtfsync](rtfsync.md)関数を呼び出して、テキストと書式を同期します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="0d8f4-140">これは新しいメッセージなので、RTF_SYNC_RTF_CHANGED と RTF_SYNC_BODY_CHANGED の両方のフラグを設定して、RTF 形式とテキスト形式のメッセージテキストの両方が変更されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="0d8f4-141">**rtfsync**は、メッセージストアプロバイダーが必要とするいくつかの関連するプロパティ ( **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) など) を設定し、メッセージに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="0d8f4-142">変更をコミットしてメモリを解放するため、 **IStream:: commit**および**IUnknown:: Release**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0d8f4-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

