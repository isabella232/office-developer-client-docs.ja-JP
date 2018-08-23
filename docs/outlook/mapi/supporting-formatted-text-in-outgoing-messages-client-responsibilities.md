---
title: 送信メッセージ クライアントの責任で書式設定されたテキストをサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d5ce2e6b0f10ff6c2f6fd91ca9f73953f3ee7cd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804027"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="a2b62-103">送信メッセージでの書式付きテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="a2b62-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="a2b62-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2b62-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2b62-105">クライアント アプリケーションは、([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティ、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティ、または送信メッセージの**PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="a2b62-106">プレーン テキストのみをサポートするクライアントは、 **PR_BODY**プロパティのみを設定します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="a2b62-107">リッチ テキスト形 (式 RTF) のクライアント設定**PR_BODY**と**PR_RTF_COMPRESSED**プロパティの両方、またはのみ**PR_RTF_COMPRESSED**、メッセージによって使用されているプロバイダーを格納するに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a2b62-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="a2b62-108">HTML に対応していないクライアントは、 **PR_HTML**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="a2b62-109">クライアント ストアが RTF をサポートしているかどうかを判断するのには、メッセージ ・ ストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティをチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2b62-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="a2b62-110">メッセージ ・ ストアが RTF に対応していない場合、rtf 形式に対応していないクライアントは、各送信メッセージの**PR_BODY**と**PR_RTF_COMPRESSED**の両方のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="a2b62-111">メッセージ ・ ストアが RTF に対応していない場合は、 **PR_RTF_COMPRESSED**プロパティのみを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2b62-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="a2b62-112">**必要に応じて、rtf 形式に対応したクライアントとして PR_RTF_COMPRESSED を設定し、同期を確実に処理が行われます**</span><span class="sxs-lookup"><span data-stu-id="a2b62-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="a2b62-113">タグと MAPI_MODIFY フラグを設定、 **PR_RTF_COMPRESSED**プロパティを開くには、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="a2b62-114">タグでは、古いデータが新しいデータに置き換えられ、MAPI_MODIFY を使用すると、これらの置換を行うことを保証します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="a2b62-115">関数を呼び出す、 [WrapCompressedRTFStream](wrapcompressedrtfstream.md) STORE_UNCOMPRESSED_RTF、メッセージ ・ ストア**PR_RTF_COMPRESSED の非圧縮のバージョンを取得するのには、 **PR_STORE_SUPPORT_MASK**プロパティに STORE_UNCOMPRESSED_RTF ビットを設定する場合** **OpenProperty**からストリームが返されます。</span><span class="sxs-lookup"><span data-stu-id="a2b62-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="a2b62-116">**WrapCompressedRTFStream**から返される非圧縮ストリームをメッセージのテキスト データを記述します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="a2b62-117">コミットし、非圧縮と圧縮の両方のストリームを解放します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="a2b62-118">この時点で、メッセージ ストア プロバイダーは、rtf 形式をサポートする場合に必要なすべてが行われます。</span><span class="sxs-lookup"><span data-stu-id="a2b62-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="a2b62-119">必要な場合はメッセージ ストア プロバイダーは、同期処理と**PR_BODY**プロパティの作成処理に依存することができます。</span><span class="sxs-lookup"><span data-stu-id="a2b62-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="a2b62-120">ただし、メッセージ ストア プロバイダーが RTF をサポートしていない場合を呼び出す必要があります、書式設定されたテキストの同期を[行う](rtfsync.md)関数 RTF_SYNC_RTF_CHANGED フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="a2b62-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

