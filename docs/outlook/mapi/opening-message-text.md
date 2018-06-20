---
title: 開始メッセージのテキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801689"
---
# <a name="opening-message-text"></a><span data-ttu-id="6b7e3-103">開始メッセージのテキスト</span><span class="sxs-lookup"><span data-stu-id="6b7e3-103">Opening message text</span></span>

<span data-ttu-id="6b7e3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b7e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b7e3-105">メッセージのテキストが格納されているいずれかでその**PR\_本文**プロパティまたは**PR\_RTF\_圧縮**プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="6b7e3-106">詳細についてを参照してください**PR\_本体**([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) と**PR\_RTF\_圧縮**([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="6b7e3-107">リッチ テキスト形式 (RTF) をサポートする場合を開く**PR\_RTF_COMPRESSED**。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="6b7e3-108">RTF がサポートしていない場合は開きます**PR\_本文**。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="6b7e3-109">メッセージのテキストであるために設定されているかどうかに関係なく大きい、これらのプロパティを開くに**IMAPIProp::OpenProperty**を使用します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="6b7e3-110">詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="6b7e3-111">書式設定されたメッセージのテキストを表示するには</span><span class="sxs-lookup"><span data-stu-id="6b7e3-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="6b7e3-112">場合は、ストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティに STORE_RTF_OK フラグがない場合で示されるように、rtf 形式以外の注意のメッセージ ・ ストアを使用しています。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="6b7e3-113">**PR_RTF_IN_SYNC**プロパティを取得するために、メッセージの**IMAPIProp::GetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="6b7e3-114">詳細については、 [IMAPIProp::GetProps](imapiprop-getprops.md)と**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="6b7e3-115">**PR_RTF_COMPRESSED**プロパティを使用してメッセージの PR_BODY プロパティの同期を行うを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="6b7e3-116">詳細については、[行う](rtfsync.md) **PR_BODY**、 **PR_RTF_COMPRESSED**を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="6b7e3-117">パスのプロパティが存在しないために、 **PR_RTF_IN_SYNC**を取得する呼び出しが失敗した場合、RTF_SYNC_BODY_CHANGED フラグを設定またはそれが FALSE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="6b7e3-118">**行う**には、TRUE が返された場合、変更が加えられたことを示す-永続的にそれらを保存するのには、メッセージの**IMAPIProp::SaveChanges**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="6b7e3-119">詳細については、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="6b7e3-120">RTF に対応していないメッセージを使用するかどうかに関係なく次のように保存します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="6b7e3-121">**PR_RTF_COMPRESSED**プロパティを開くには、 **IMAPIProp::OpenProperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="6b7e3-122">詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **PR_RTF_COMPRESSED**を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="6b7e3-123">**PR_RTF_COMPRESSED**が利用できない場合は、 **PR_BODY**プロパティを開くには、 **OpenProperty**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="6b7e3-124">使用可能な場合は、圧縮された rtf 形式のデータの圧縮されていないバージョンを作成する**WrapCompressedRTFStream**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="6b7e3-125">詳細については、 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="6b7e3-126">ストリームから書式付きの文字列をメッセージ フォームで適切な位置にコピーします。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="6b7e3-127">プレーン テキスト メッセージのテキストを表示するには</span><span class="sxs-lookup"><span data-stu-id="6b7e3-127">To display plain message text</span></span>
  
1. <span data-ttu-id="6b7e3-128">**PR_BODY**プロパティを取得するために、メッセージの**IMAPIProp::GetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="6b7e3-129">詳細については、 [IMAPIProp::GetProps](imapiprop-getprops.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="6b7e3-130">**GetProps**には、プロパティ値の構造体または MAPI_E_NOT_ENOUGH_MEMORY のプロパティの型のいずれかの PT_ERROR が返された場合は、メッセージの**IMAPIProp::OpenProperty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="6b7e3-131">プロパティ タグとインターフェイス識別子として IID_IStream として**PR_BODY**を渡します。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="6b7e3-132">詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="6b7e3-133">メッセージ フォーム内の適切な位置にストリームからプレーン テキストをコピーします。</span><span class="sxs-lookup"><span data-stu-id="6b7e3-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

