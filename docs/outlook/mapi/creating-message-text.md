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
# <a name="creating-message-text"></a><span data-ttu-id="d6031-103">メッセージ テキストの作成</span><span class="sxs-lookup"><span data-stu-id="d6031-103">Creating message text</span></span>

<span data-ttu-id="d6031-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6031-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6031-105">一部のメッセージは受信者リストと件名行で構成されていますが、ほとんどのメッセージの内容 、特に IPM です。メモ メッセージには、テキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d6031-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="d6031-106">メッセージ テキストはプレーンまたは書式設定され **、PR \_ BODY** [(PidTagBody)、PR](pidtagbody-canonical-property.md) **\_ HTML** [(PidTagHtml)、](pidtaghtml-canonical-property.md)および PR_RTF_COMPRESSED [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)の **3 つのプロパティに** 格納されます。</span><span class="sxs-lookup"><span data-stu-id="d6031-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="d6031-107">クライアントがプレーン テキスト ベースの場合は **、PR BODY を設定 \_ します**。</span><span class="sxs-lookup"><span data-stu-id="d6031-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="d6031-108">リッチ テキスト形式 (RTF) で書式設定されたテキストをサポートしている場合は、使用しているメッセージ ストア プロバイダーに応じて **、PR_RTF_COMPRESSED** のみ、または **PR_RTF_COMPRESSED** と **PR \_ BODY** の両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="d6031-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="d6031-109">RTF 対応クライアントが RTF 対応のメッセージ ストアを使用している場合、RTF 対応 **のPR_RTF_COMPRESSED** 設定します。</span><span class="sxs-lookup"><span data-stu-id="d6031-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="d6031-110">RTF 対応クライアントが RTF 対応以外のメッセージ ストアを使用している場合は、両方のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d6031-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="d6031-111">クライアントが HTML をサポートしている場合は、PR_HTMLプロパティ **を設定** します。</span><span class="sxs-lookup"><span data-stu-id="d6031-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="d6031-112">メッセージ ストアでリッチ テキスト形式がサポートされているかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="d6031-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="d6031-113">メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d6031-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="d6031-114">このビットをSTORE_RTF_OKします。</span><span class="sxs-lookup"><span data-stu-id="d6031-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="d6031-115">このSTORE_RTF_OK設定されている場合、メッセージ ストア プロバイダーは RTF テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d6031-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="d6031-116">設定されていない場合、メッセージ ストア プロバイダーはプレーン テキストのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d6031-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="d6031-117">メッセージ ストアが HTML をサポートするかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="d6031-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="d6031-118">メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_STORE_SUPPORT_MASK **取得します** 。</span><span class="sxs-lookup"><span data-stu-id="d6031-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="d6031-119">ビットをSTORE_HTML_OKします。</span><span class="sxs-lookup"><span data-stu-id="d6031-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="d6031-120">このSTORE_HTML_OK設定されている場合、メッセージ ストア プロバイダーは HTML テキストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d6031-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-pr_rtf_compressed"></a><span data-ttu-id="d6031-121">PR の設定RTF_COMPRESSED \_</span><span class="sxs-lookup"><span data-stu-id="d6031-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="d6031-122">メッセージの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出して **、PR_RTF_COMPRESSED** プロパティを開き、IID_IStream をインターフェイス識別子として指定し、MAPI_CREATE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d6031-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="d6031-123">メッセージ ストアの PR_STORE_SUPPORT_MASK プロパティで STORE_UNCOMPRESSED_RTF ビットが設定されている場合は [、wrapCompressedRTFStream](wrapcompressedrtfstream.md) 関数を呼び出し、STORE_UNCOMPRESSED_RTF フラグ **を渡** します。</span><span class="sxs-lookup"><span data-stu-id="d6031-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="d6031-124">元のストリームを解放するには、 \*\* IUnknown::Release \*\* メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d6031-124">Release the original stream by calling its \*\* IUnknown::Release \*\* method.</span></span> 
    
4. <span data-ttu-id="d6031-125">\*\* IStream::Write \*\* または **IStream::CopyTo** を呼び出して **、WrapCompressedRTFStream** から返されるストリームにメッセージ テキストを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="d6031-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="d6031-126">OpenProperty **メソッド\*\*\*\*から** 返されるストリームの Commit メソッドと Release メソッド **を呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="d6031-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="d6031-127">この時点で、メッセージ ストア プロバイダーが RTF をサポートしている場合は、必要なすべての処理を行いました。</span><span class="sxs-lookup"><span data-stu-id="d6031-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="d6031-128">メッセージ のコンテンツと書式設定の同期を処理し、必要に応じて **PR \_ BODY** プロパティを作成するには、メッセージ ストア プロバイダーに依存できます。</span><span class="sxs-lookup"><span data-stu-id="d6031-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="d6031-129">RTF 対応のメッセージ ストアは、 [同期を処理するために RTFSync](rtfsync.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d6031-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="d6031-130">RTF フラグSYNC_BODY_CHANGED TRUE に設定されている場合、プロバイダーは PR_BODY \_ プロパティ **をPR_BODY** します。</span><span class="sxs-lookup"><span data-stu-id="d6031-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="d6031-131">メッセージ ストア プロバイダーが RTF をサポートしていない場合は、PR_BODY プロパティを設定して RTF 以外 **のメッセージ コンテンツを追加する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="d6031-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-pr_html"></a><span data-ttu-id="d6031-132">設定PR_HTML</span><span class="sxs-lookup"><span data-stu-id="d6031-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="d6031-133">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IStream** インターフェイス **PR_HTMLプロパティ** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d6031-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="d6031-134">OpenProperty から返されるストリームにメッセージ テキスト データを書き込む **には、IStream::Write を呼び出します**。 </span><span class="sxs-lookup"><span data-stu-id="d6031-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="d6031-135">**IStream::Commit と** **IUnknown::Release** on the stream を呼び出して、変更をコミットし、そのメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="d6031-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-pr_body"></a><span data-ttu-id="d6031-136">設定PR_BODY</span><span class="sxs-lookup"><span data-stu-id="d6031-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="d6031-137">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IStream** インターフェイスで **PR_BODYプロパティ** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d6031-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="d6031-138">OpenProperty から返されるストリームにメッセージ テキスト データを書き込む **には、IStream::Write を呼び出します**。 </span><span class="sxs-lookup"><span data-stu-id="d6031-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="d6031-139">[RTFSync 関数を呼び出](rtfsync.md)して、テキストを書式設定と同期します。</span><span class="sxs-lookup"><span data-stu-id="d6031-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="d6031-140">これは新しいメッセージなので、RTF_SYNC_RTF_CHANGED フラグと RTF_SYNC_BODY_CHANGED フラグの両方を設定して、メッセージ テキストの RTF とプレーン テキストの両方のバージョンが変更されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d6031-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="d6031-141">**RTFSync** は、PR_RTF_IN_SYNC ([PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)など、メッセージ ストア プロバイダーが必要とするいくつかの関連プロパティを設定し、メッセージに書き込みます。 </span><span class="sxs-lookup"><span data-stu-id="d6031-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="d6031-142">**IStream::Commit と** **IUnknown::Release** on the stream を呼び出して、変更をコミットし、そのメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="d6031-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

