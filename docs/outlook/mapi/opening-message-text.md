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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407537"
---
# <a name="opening-message-text"></a><span data-ttu-id="bb6dd-103">メッセージ テキストを開く</span><span class="sxs-lookup"><span data-stu-id="bb6dd-103">Opening message text</span></span>

<span data-ttu-id="bb6dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb6dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb6dd-105">メッセージのテキストは、PR **\_ BODY** プロパティまたは PR **\_ RTF \_ COMPRESSED プロパティに格納** されます。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="bb6dd-106">詳細については **、「PR \_ BODY** [(PidTagBody)」、PR](pidtagbody-canonical-property.md) **\_ HTML** [(PidTagHtml)、PR](pidtaghtml-canonical-property.md) **RTF \_ \_ COMPRESSED** [(PidTagRtfCompressed)を参照してください](pidtagrtfcompressed-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="bb6dd-107">リッチ テキスト形式 (RTF) をサポートしている場合は **、PR ファイルを \_ 開** RTF_COMPRESSED。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="bb6dd-108">RTF をサポートしていない場合は **、PR BODY を \_ 開きます**。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="bb6dd-109">メッセージのテキストは、書式が設定されているかどうかに関係なく大きくすることができますので **、IMAPIProp::OpenProperty** を使用してこれらのプロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="bb6dd-110">詳細については [、「IMAPIProp::OpenProperty」を参照してください](imapiprop-openproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="bb6dd-111">書式設定されたメッセージ テキストを表示するには</span><span class="sxs-lookup"><span data-stu-id="bb6dd-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="bb6dd-112">RTF 対応以外のメッセージ ストアを使用している場合は、ストアの PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに STORE_RTF_OK フラグがない場合に示されます。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="bb6dd-113">メッセージの **IMAPIProp::GetProps** メソッドを呼び出して、PR_RTF_IN_SYNC **取得します** 。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="bb6dd-114">詳細については[、「IMAPIProp::GetProps](imapiprop-getprops.md) and PR_RTF_IN_SYNC ([PidTagRtfInSync)」を参照してください](pidtagrtfinsync-canonical-property.md)。 </span><span class="sxs-lookup"><span data-stu-id="bb6dd-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="bb6dd-115">RTFSync を呼び出して、メッセージの PR_BODY プロパティを **PR_RTF_COMPRESSEDします** 。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="bb6dd-116">詳細については [、「RTFSync、PR_BODY、](rtfsync.md)および **PR_RTF_COMPRESSED」\*\*\*\*を参照してください**。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="bb6dd-117">プロパティがRTF_SYNC_BODY_CHANGED、または FALSE に設定されているPR_RTF_IN_SYNCを取得する呼び出しが失敗した場合は、このフラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="bb6dd-118">**RTFSync が** TRUE を返した場合 (変更が行われたことを示す) 場合は、メッセージの **IMAPIProp::SaveChanges** メソッドを呼び出して、それらを完全に保存します。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="bb6dd-119">詳細については [、「IMAPIProp::SaveChanges」を参照してください](imapiprop-savechanges.md)。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="bb6dd-120">RTF 対応のメッセージ ストアを使用しているかどうかに関係なく、次の点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="bb6dd-121">**IMAPIProp::OpenProperty** を呼び出して、次のプロパティ **PR_RTF_COMPRESSED** します。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="bb6dd-122">詳細については [、「IMAPIProp::OpenProperty」および「PR_RTF_COMPRESSED」](imapiprop-openproperty.md) を **参照してください**。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="bb6dd-123">この **PR_RTF_COMPRESSED** 使用できない場合は **、OpenProperty を** 呼び出してプロパティを **開** PR_BODYします。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="bb6dd-124">**WrapCompressedRTFStream** 関数を呼び出して、圧縮された RTF データの圧縮されていないバージョンを作成します (使用可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="bb6dd-125">詳細については [、「WrapCompressedRTFStream」を参照してください](wrapcompressedrtfstream.md)。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="bb6dd-126">メッセージ フォーム内の適切な場所に、ストリームから書式設定されたテキストをコピーします。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="bb6dd-127">プレーン メッセージ テキストを表示するには</span><span class="sxs-lookup"><span data-stu-id="bb6dd-127">To display plain message text</span></span>
  
1. <span data-ttu-id="bb6dd-128">メッセージの **IMAPIProp::GetProps** メソッドを呼び出して、PR_BODY **取得します** 。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="bb6dd-129">詳細については [、「IMAPIProp::GetProps」を参照してください](imapiprop-getprops.md)。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="bb6dd-130">**GetProps** がプロパティPT_ERROR構造体または MAPI_E_NOT_ENOUGH_MEMORY のプロパティの種類のプロパティを返す場合は、メッセージの **IMAPIProp::OpenProperty** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="bb6dd-131">プロパティ **PR_BODY** として渡し、IID_IStream識別子として渡します。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="bb6dd-132">詳細については [、「IMAPIProp::OpenProperty」を参照してください](imapiprop-openproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="bb6dd-133">ストリームからメッセージ フォーム内の適切な場所にプレーン テキストをコピーします。</span><span class="sxs-lookup"><span data-stu-id="bb6dd-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

