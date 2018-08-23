---
title: テキスト形式での添付ファイルの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 031f8f17ae98bd62043a2cd8ce6c8c2d55a19c9f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582337"
---
# <a name="rendering-an-attachment-in-plain-text"></a><span data-ttu-id="a7719-103">テキスト形式での添付ファイルの表示</span><span class="sxs-lookup"><span data-stu-id="a7719-103">Rendering an Attachment in Plain Text</span></span>

  
  
<span data-ttu-id="a7719-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7719-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7719-105">レンダリングするテキスト形式のメッセージで添付ファイル添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティを取得し、 **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) 内のデータに適用します。プロパティです。</span><span class="sxs-lookup"><span data-stu-id="a7719-105">To render an attachment in a message with plain text, retrieve the attachment's **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property and apply it to the data in the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property.</span></span> <span data-ttu-id="a7719-106">**PR_RENDERING_POSITION**を取得する 2 とおりの方法があります。</span><span class="sxs-lookup"><span data-stu-id="a7719-106">There are two ways to retrieve **PR_RENDERING_POSITION**:</span></span>
  
- <span data-ttu-id="a7719-107">メッセージの**IMessage::OpenAttach**メソッドを呼び出すことによって、添付ファイルを開くし、 **PR_RENDERING_POSITION**プロパティの添付ファイルの**IMAPIProp::GetProps**メソッドを呼び出すことによって。</span><span class="sxs-lookup"><span data-stu-id="a7719-107">Open the attachment by calling the message's **IMessage::OpenAttach** method and then ask for the **PR_RENDERING_POSITION** property by calling the attachment's **IMAPIProp::GetProps** method.</span></span> <span data-ttu-id="a7719-108">詳細については、 [IMessage::OpenAttach](imessage-openattach.md)および[IMAPIProp::GetProps](imapiprop-getprops.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7719-108">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
- <span data-ttu-id="a7719-109">メソッドを呼び出してメッセージの**IMessage::GetAttachmentTable**を添付ファイル テーブルにアクセスし、 **PR_RENDERING_POSITION**プロパティを保持する列を取得します。</span><span class="sxs-lookup"><span data-stu-id="a7719-109">Call the message's **IMessage::GetAttachmentTable** method to access its attachment table and retrieve the column that holds the **PR_RENDERING_POSITION** property.</span></span> <span data-ttu-id="a7719-110">この方法は、常に推奨します。</span><span class="sxs-lookup"><span data-stu-id="a7719-110">This way is always preferable.</span></span> <span data-ttu-id="a7719-111">詳細については、 [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7719-111">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
<span data-ttu-id="a7719-112">RTF に対応していない多くのメッセージ ストアを計算しない**PR_RENDERING_POSITION**クライアントは、メッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のプロパティを要求するまでに留意してください。</span><span class="sxs-lookup"><span data-stu-id="a7719-112">Keep in mind that many RTF-aware message stores do not calculate **PR_RENDERING_POSITION** until a client requests the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of a message.</span></span> <span data-ttu-id="a7719-113">それまでは、 **PR_RENDERING_POSITION**は、通常、概算値を表します。</span><span class="sxs-lookup"><span data-stu-id="a7719-113">Until that time, **PR_RENDERING_POSITION** usually represents an approximate value.</span></span> <span data-ttu-id="a7719-114">メッセージ ストア プロバイダーは、パフォーマンスを強化するために概算値をクライアントに提供できるのです。</span><span class="sxs-lookup"><span data-stu-id="a7719-114">Message store providers are allowed to supply clients with an approximate value to enhance performance.</span></span> 
  
<span data-ttu-id="a7719-115">ファイルまたはバイナリ添付ファイルのレンダリングは、その**PR_ATTACH_RENDERING**プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="a7719-115">The rendering for a file or binary attachment is stored in its **PR_ATTACH_RENDERING** property.</span></span> <span data-ttu-id="a7719-116">**PR_RENDERING_POSITION**を取得するのと同じ方法で**PR_ATTACH_RENDERING**を取得する選択がある: 添付ファイルや添付ファイル テーブルから直接。</span><span class="sxs-lookup"><span data-stu-id="a7719-116">You have the choice of retrieving **PR_ATTACH_RENDERING** in the same ways as you retrieved **PR_RENDERING_POSITION**: directly from the attachment or from the attachment table.</span></span> <span data-ttu-id="a7719-117">**PR_ATTACH_RENDERING**、最初の方法のですより時間がかかる方が安全です。</span><span class="sxs-lookup"><span data-stu-id="a7719-117">For **PR_ATTACH_RENDERING**, the first strategy, although more time-consuming, is safer.</span></span> <span data-ttu-id="a7719-118">メッセージ ストア プロバイダーの中では、255 バイト、または 510 バイトまでのいくつかの場合、テーブルの列を切り捨て、ためには、 **PR_ATTACH_RENDERING**列に完全なレンダリングが含まれていることを確認することは困難です。</span><span class="sxs-lookup"><span data-stu-id="a7719-118">Because some message store providers truncate their table columns to 255 bytes, or in a few cases 510 bytes, it is difficult to be sure that the **PR_ATTACH_RENDERING** column contains the complete rendering.</span></span> <span data-ttu-id="a7719-119">添付ファイルから直接プロパティを検索する場合に常に完了となります。</span><span class="sxs-lookup"><span data-stu-id="a7719-119">When retrieving the property directly from the attachment, it will always be complete.</span></span> 
  
<span data-ttu-id="a7719-120">OLE もメッセージの添付ファイルは、 **PR_ATTACH_RENDERING**を設定します。</span><span class="sxs-lookup"><span data-stu-id="a7719-120">Neither OLE nor message attachments set **PR_ATTACH_RENDERING**.</span></span> <span data-ttu-id="a7719-121">代わりに、OLE 1 の添付ファイルの表示については、メッセージのテキスト ストリームに格納されます。</span><span class="sxs-lookup"><span data-stu-id="a7719-121">Instead, rendering information for OLE 1 attachments is stored in the message text stream.</span></span> <span data-ttu-id="a7719-122">OLE 2 の添付ファイルの記憶域オブジェクトの子の特別なストリームに格納されます。</span><span class="sxs-lookup"><span data-stu-id="a7719-122">For OLE 2 attachments, it is stored in a special child stream of the storage object.</span></span> <span data-ttu-id="a7719-123">メッセージの添付ファイルの情報を表示、フォーム マネージャーを通じて利用可能です。</span><span class="sxs-lookup"><span data-stu-id="a7719-123">Rendering information for message attachments is available through the form manager.</span></span> 
  
 <span data-ttu-id="a7719-124">**メッセージの添付ファイルのレンダリングを取得するには**</span><span class="sxs-lookup"><span data-stu-id="a7719-124">**To retrieve the rendering for a message attachment**</span></span>
  
1. <span data-ttu-id="a7719-125">フォーム マネージャーにアクセスするのにには、メッセージのメッセージ クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="a7719-125">Use the message class of the message to access the form manager.</span></span>
    
2. <span data-ttu-id="a7719-126">フォーム マネージャーの**PR_MINI_ICON**プロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="a7719-126">Access the form manager's **PR_MINI_ICON** property.</span></span> <span data-ttu-id="a7719-127">詳細については、 **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7719-127">For more information, see **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span></span>
    

