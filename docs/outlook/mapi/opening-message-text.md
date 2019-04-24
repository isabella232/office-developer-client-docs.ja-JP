---
title: メッセージ テキストを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348581"
---
# <a name="opening-message-text"></a><span data-ttu-id="94d61-103">メッセージ テキストを開く</span><span class="sxs-lookup"><span data-stu-id="94d61-103">Opening message text</span></span>

<span data-ttu-id="94d61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94d61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94d61-105">メッセージのテキストは、 **pr\_BODY**プロパティまたは**\_pr RTF\_圧縮**プロパティのどちらかに格納されます。</span><span class="sxs-lookup"><span data-stu-id="94d61-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="94d61-106">詳細については **、\_「pr BODY** ([PidTagBody](pidtagbody-canonical-property.md))」、「 **\_pr HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))」、および「 **pr\_RTF\_圧縮**([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="94d61-107">リッチテキスト形式 (RTF) をサポートしている場合は、 **PR\_RTF_COMPRESSED**を開きます。</span><span class="sxs-lookup"><span data-stu-id="94d61-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="94d61-108">RTF をサポートしていない場合は、 **PR\_本文**を開きます。</span><span class="sxs-lookup"><span data-stu-id="94d61-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="94d61-109">メッセージのテキストは、書式設定されているかどうかに関係なく大きくなる可能性があるため、 **imapiprop:: openproperty**を使用してこれらのプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="94d61-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="94d61-110">詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="94d61-111">書式設定されたメッセージテキストを表示するには</span><span class="sxs-lookup"><span data-stu-id="94d61-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="94d61-112">RTF に対応しないメッセージストアを使用している場合は、ストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに STORE_RTF_OK フラグがないことが示されます。</span><span class="sxs-lookup"><span data-stu-id="94d61-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="94d61-113">メッセージの**imapiprop:: GetProps**メソッドを呼び出して、 **PR_RTF_IN_SYNC**プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="94d61-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="94d61-114">詳細については、「 [imapiprop:: GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="94d61-115">rtfsync を呼び出して、メッセージの PR_BODY プロパティを**PR_RTF_COMPRESSED**プロパティと同期します。</span><span class="sxs-lookup"><span data-stu-id="94d61-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="94d61-116">詳細については、「 [rtfsync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="94d61-117">プロパティが存在しないか FALSE に設定されているため、 **PR_RTF_IN_SYNC**を取得する呼び出しが失敗した場合は、RTF_SYNC_BODY_CHANGED フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="94d61-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="94d61-118">**rtfsync**が TRUE を返した場合—変更が行われたことを示す、メッセージの**imapiprop:: SaveChanges**メソッドを呼び出して永続的に保存します。</span><span class="sxs-lookup"><span data-stu-id="94d61-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="94d61-119">詳細については、「 [imapiprop:: SaveChanges](imapiprop-savechanges.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="94d61-120">RTF 対応のメッセージストアを使用しているかどうかに関係なく、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="94d61-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="94d61-121">**PR_RTF_COMPRESSED**プロパティを開くには、 **imapiprop:: openproperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="94d61-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="94d61-122">詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="94d61-123">**PR_RTF_COMPRESSED**が使用できない場合は、 **openproperty**を呼び出して**PR_BODY**プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="94d61-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="94d61-124">圧縮された RTF データの圧縮されていないバージョンを作成するには、 **WrapCompressedRTFStream**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="94d61-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="94d61-125">詳細については、「 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="94d61-126">書式設定されたテキストを stream からメッセージフォームの適切な位置にコピーします。</span><span class="sxs-lookup"><span data-stu-id="94d61-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="94d61-127">テキスト形式のメッセージテキストを表示するには</span><span class="sxs-lookup"><span data-stu-id="94d61-127">To display plain message text</span></span>
  
1. <span data-ttu-id="94d61-128">メッセージの**imapiprop:: GetProps**メソッドを呼び出して、 **PR_BODY**プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="94d61-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="94d61-129">詳細については、「 [imapiprop:: GetProps](imapiprop-getprops.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="94d61-130">プロパティの値の構造体または MAPI_E_NOT_ENOUGH_MEMORY でプロパティの型の PT_ERROR が返された場合、 **GetProps**はメッセージの**imapiprop:: openproperty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="94d61-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="94d61-131">**PR_BODY**をプロパティタグとして、IID_IStream をインターフェイス識別子として渡します。</span><span class="sxs-lookup"><span data-stu-id="94d61-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="94d61-132">詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94d61-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="94d61-133">ストリームからメッセージフォームの適切な位置にプレーンテキストをコピーします。</span><span class="sxs-lookup"><span data-stu-id="94d61-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

