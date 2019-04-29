---
title: テキスト形式での添付ファイルのレンダリング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410876"
---
# <a name="rendering-an-attachment-in-plain-text"></a><span data-ttu-id="2e9d7-103">テキスト形式での添付ファイルのレンダリング</span><span class="sxs-lookup"><span data-stu-id="2e9d7-103">Rendering an Attachment in Plain Text</span></span>

  
  
<span data-ttu-id="2e9d7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e9d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e9d7-105">テキスト形式のメッセージに添付ファイルを表示するには、添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティを取得し、 **PR_ATTACH_RENDERING**のデータに適用します ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))。プロパティ.</span><span class="sxs-lookup"><span data-stu-id="2e9d7-105">To render an attachment in a message with plain text, retrieve the attachment's **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property and apply it to the data in the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property.</span></span> <span data-ttu-id="2e9d7-106">**PR_RENDERING_POSITION**を取得するには、次の2つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-106">There are two ways to retrieve **PR_RENDERING_POSITION**:</span></span>
  
- <span data-ttu-id="2e9d7-107">メッセージの**IMessage:: openattach**メソッドを呼び出して添付ファイルを開き、添付ファイルの**imapiprop:: GetProps**メソッドを呼び出して**PR_RENDERING_POSITION**プロパティを要求します。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-107">Open the attachment by calling the message's **IMessage::OpenAttach** method and then ask for the **PR_RENDERING_POSITION** property by calling the attachment's **IMAPIProp::GetProps** method.</span></span> <span data-ttu-id="2e9d7-108">詳細については、「 [IMessage:: openattach](imessage-openattach.md) and [imapiprop:: GetProps](imapiprop-getprops.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-108">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
- <span data-ttu-id="2e9d7-109">メッセージの**IMessage:: getattachmenttable**メソッドを呼び出して、その添付ファイルテーブルにアクセスし、 **PR_RENDERING_POSITION**プロパティを保持する列を取得します。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-109">Call the message's **IMessage::GetAttachmentTable** method to access its attachment table and retrieve the column that holds the **PR_RENDERING_POSITION** property.</span></span> <span data-ttu-id="2e9d7-110">この方法は常に推奨されます。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-110">This way is always preferable.</span></span> <span data-ttu-id="2e9d7-111">詳細については、「 [IMessage:: getattachmenttable](imessage-getattachmenttable.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-111">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
<span data-ttu-id="2e9d7-112">RTF 対応メッセージストアの多くは、クライアントがメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティを要求するまで**PR_RENDERING_POSITION**を計算しないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-112">Keep in mind that many RTF-aware message stores do not calculate **PR_RENDERING_POSITION** until a client requests the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of a message.</span></span> <span data-ttu-id="2e9d7-113">その時点まで、 **PR_RENDERING_POSITION**は通常近似値を表します。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-113">Until that time, **PR_RENDERING_POSITION** usually represents an approximate value.</span></span> <span data-ttu-id="2e9d7-114">メッセージストアプロバイダーは、パフォーマンスを向上させるために概数値をクライアントに提供できます。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-114">Message store providers are allowed to supply clients with an approximate value to enhance performance.</span></span> 
  
<span data-ttu-id="2e9d7-115">ファイルまたはバイナリ添付ファイルのレンダリングは、 **PR_ATTACH_RENDERING**プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-115">The rendering for a file or binary attachment is stored in its **PR_ATTACH_RENDERING** property.</span></span> <span data-ttu-id="2e9d7-116">**PR_RENDERING_POSITION**を取得した場合と同じ方法で**PR_ATTACH_RENDERING**を取得する方法として、添付ファイルまたは添付ファイルテーブルから直接取得する方法があります。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-116">You have the choice of retrieving **PR_ATTACH_RENDERING** in the same ways as you retrieved **PR_RENDERING_POSITION**: directly from the attachment or from the attachment table.</span></span> <span data-ttu-id="2e9d7-117">**PR_ATTACH_RENDERING**の場合、最初の戦略は時間がかかることもありますが、より安全です。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-117">For **PR_ATTACH_RENDERING**, the first strategy, although more time-consuming, is safer.</span></span> <span data-ttu-id="2e9d7-118">一部のメッセージストアプロバイダーでは、表の列が255バイトに切り捨てられるか、場合によっては510バイトで切り捨てられることがあるため、 **PR_ATTACH_RENDERING**列に完全なレンダリングが含まれていることを確認するのは困難です。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-118">Because some message store providers truncate their table columns to 255 bytes, or in a few cases 510 bytes, it is difficult to be sure that the **PR_ATTACH_RENDERING** column contains the complete rendering.</span></span> <span data-ttu-id="2e9d7-119">添付ファイルから直接プロパティを取得する場合は、常に完了します。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-119">When retrieving the property directly from the attachment, it will always be complete.</span></span> 
  
<span data-ttu-id="2e9d7-120">OLE もメッセージ添付ファイルも**PR_ATTACH_RENDERING**に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-120">Neither OLE nor message attachments set **PR_ATTACH_RENDERING**.</span></span> <span data-ttu-id="2e9d7-121">代わりに、OLE 1 添付ファイルのレンダリング情報は、メッセージテキストストリームに格納されます。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-121">Instead, rendering information for OLE 1 attachments is stored in the message text stream.</span></span> <span data-ttu-id="2e9d7-122">OLE 2 の添付ファイルの場合は、ストレージオブジェクトの特別な子ストリームに格納されます。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-122">For OLE 2 attachments, it is stored in a special child stream of the storage object.</span></span> <span data-ttu-id="2e9d7-123">メッセージの添付ファイルのレンダリング情報は、フォームマネージャーから使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-123">Rendering information for message attachments is available through the form manager.</span></span> 
  
 <span data-ttu-id="2e9d7-124">**メッセージの添付ファイルのレンダリングを取得するには**</span><span class="sxs-lookup"><span data-stu-id="2e9d7-124">**To retrieve the rendering for a message attachment**</span></span>
  
1. <span data-ttu-id="2e9d7-125">フォームマネージャーにアクセスするには、メッセージのメッセージクラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-125">Use the message class of the message to access the form manager.</span></span>
    
2. <span data-ttu-id="2e9d7-126">フォームマネージャーの**PR_MINI_ICON**プロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-126">Access the form manager's **PR_MINI_ICON** property.</span></span> <span data-ttu-id="2e9d7-127">詳細については、「 **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e9d7-127">For more information, see **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span></span>
    

