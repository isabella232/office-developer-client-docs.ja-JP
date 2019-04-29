---
title: 送信メッセージの書式付きテキストのサポートクライアントの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431604"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="3b218-103">送信メッセージでの書式付きテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="3b218-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="3b218-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b218-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b218-105">クライアントアプリケーションは、送信メッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティ、または**PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3b218-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="3b218-106">プレーンテキストのみをサポートするクライアントは、 **PR_BODY**プロパティのみを設定します。</span><span class="sxs-lookup"><span data-stu-id="3b218-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="3b218-107">リッチテキスト形式 (RTF) 対応クライアントは、使用されているメッセージストアプロバイダーに応じて、 **PR_BODY**と**PR_RTF_COMPRESSED**の両方のプロパティを設定するか、または**PR_RTF_COMPRESSED**のみを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3b218-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="3b218-108">HTML 対応クライアントは、 **PR_HTML**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3b218-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="3b218-109">クライアントがメッセージストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティをチェックして、ストアが RTF をサポートしているかどうかを判断することは重要です。</span><span class="sxs-lookup"><span data-stu-id="3b218-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="3b218-110">メッセージストアが rtf 対応ではない場合、rtf 対応クライアントは、各送信メッセージの**PR_BODY**プロパティと**PR_RTF_COMPRESSED**プロパティの両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="3b218-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="3b218-111">メッセージストアが RTF 対応の場合は、 **PR_RTF_COMPRESSED**プロパティのみを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b218-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="3b218-112">**PR_RTF_COMPRESSED を設定し、必要に応じて同期プロセスが実行されるようにするには、RTF 対応クライアントである必要があります。**</span><span class="sxs-lookup"><span data-stu-id="3b218-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="3b218-113">[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_RTF_COMPRESSED**プロパティを開き、MAPI_CREATE と MAPI_MODIFY の両方のフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="3b218-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="3b218-114">MAPI_CREATE では、既存のデータがすべて新しいデータに置き換えられるようにすることができます。これにより、これらの置換を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3b218-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="3b218-115">[WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出して、メッセージストアが**PR_STORE_SUPPORT_MASK**プロパティに STORE_UNCOMPRESSED_RTF ビットを設定している場合は STORE_UNCOMPRESSED_RTF を渡し、圧縮されていないバージョンの PR_RTF_COMPRESSED を取得します。 \*\*\*\* **openproperty**から返されたストリーム。</span><span class="sxs-lookup"><span data-stu-id="3b218-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="3b218-116">**WrapCompressedRTFStream**から返される非圧縮ストリームに、メッセージテキストデータを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="3b218-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="3b218-117">圧縮されていないストリームと圧縮されたストリームの両方をコミットして解放します。</span><span class="sxs-lookup"><span data-stu-id="3b218-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="3b218-118">この時点で、メッセージストアプロバイダーが RTF をサポートしている場合は、必要なすべての処理が完了しています。</span><span class="sxs-lookup"><span data-stu-id="3b218-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="3b218-119">必要に応じて、メッセージストアプロバイダーが同期プロセスを処理し、 **PR_BODY**プロパティの作成を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3b218-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="3b218-120">ただし、メッセージストアプロバイダーが RTF をサポートしていない場合は、 [rtfsync](rtfsync.md)関数を呼び出してテキストと書式設定を同期させ、RTF_SYNC_RTF_CHANGED フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b218-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

