---
title: プレーン テキストで添付ファイルをレンダリングする
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
# <a name="rendering-an-attachment-in-plain-text"></a><span data-ttu-id="dc419-103">プレーン テキストで添付ファイルをレンダリングする</span><span class="sxs-lookup"><span data-stu-id="dc419-103">Rendering an Attachment in Plain Text</span></span>

  
  
<span data-ttu-id="dc419-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc419-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc419-105">テキスト形式でメッセージ内の添付ファイルをレンダリングするには、添付ファイルの **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティを取得し **、PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) プロパティのデータに適用します。</span><span class="sxs-lookup"><span data-stu-id="dc419-105">To render an attachment in a message with plain text, retrieve the attachment's **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property and apply it to the data in the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property.</span></span> <span data-ttu-id="dc419-106">データを取得するには、次の **2 PR_RENDERING_POSITION。**</span><span class="sxs-lookup"><span data-stu-id="dc419-106">There are two ways to retrieve **PR_RENDERING_POSITION**:</span></span>
  
- <span data-ttu-id="dc419-107">メッセージの **IMessage::OpenAttach** メソッドを呼び出して添付ファイルを開き、添付ファイルの **IMAPIProp::GetProps** メソッドを呼び出して **PR_RENDERING_POSITION** プロパティを求める。</span><span class="sxs-lookup"><span data-stu-id="dc419-107">Open the attachment by calling the message's **IMessage::OpenAttach** method and then ask for the **PR_RENDERING_POSITION** property by calling the attachment's **IMAPIProp::GetProps** method.</span></span> <span data-ttu-id="dc419-108">詳細については [、「IMessage::OpenAttach」](imessage-openattach.md) および [「IMAPIProp::GetProps」を参照してください](imapiprop-getprops.md)。</span><span class="sxs-lookup"><span data-stu-id="dc419-108">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
- <span data-ttu-id="dc419-109">メッセージの **IMessage::GetAttachmentTable** メソッドを呼び出して、添付ファイル テーブルにアクセスし、PR_RENDERING_POSITION プロパティ **を保持する列を取得** します。</span><span class="sxs-lookup"><span data-stu-id="dc419-109">Call the message's **IMessage::GetAttachmentTable** method to access its attachment table and retrieve the column that holds the **PR_RENDERING_POSITION** property.</span></span> <span data-ttu-id="dc419-110">この方法は常に望ましい方法です。</span><span class="sxs-lookup"><span data-stu-id="dc419-110">This way is always preferable.</span></span> <span data-ttu-id="dc419-111">詳細については [、「IMessage::GetAttachmentTable」を参照してください](imessage-getattachmenttable.md)。</span><span class="sxs-lookup"><span data-stu-id="dc419-111">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
<span data-ttu-id="dc419-112">多くの RTF 対応メッセージ ストアは、クライアントがメッセージの **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティを要求するまで、PR_RENDERING_POSITION を計算しない点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="dc419-112">Keep in mind that many RTF-aware message stores do not calculate **PR_RENDERING_POSITION** until a client requests the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of a message.</span></span> <span data-ttu-id="dc419-113">この時間 **まで、PR_RENDERING_POSITION** は概算値を表します。</span><span class="sxs-lookup"><span data-stu-id="dc419-113">Until that time, **PR_RENDERING_POSITION** usually represents an approximate value.</span></span> <span data-ttu-id="dc419-114">メッセージ ストア プロバイダーは、パフォーマンスを向上させる近似値をクライアントに提供できます。</span><span class="sxs-lookup"><span data-stu-id="dc419-114">Message store providers are allowed to supply clients with an approximate value to enhance performance.</span></span> 
  
<span data-ttu-id="dc419-115">ファイルまたはバイナリ添付ファイルのレンダリングは、そのプロパティに **PR_ATTACH_RENDERING** されます。</span><span class="sxs-lookup"><span data-stu-id="dc419-115">The rendering for a file or binary attachment is stored in its **PR_ATTACH_RENDERING** property.</span></span> <span data-ttu-id="dc419-116">添付ファイルから直接、または添付PR_ATTACH_RENDERINGファイルを取得した場合と同じ方法で、PR_RENDERING_POSITIONを取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="dc419-116">You have the choice of retrieving **PR_ATTACH_RENDERING** in the same ways as you retrieved **PR_RENDERING_POSITION**: directly from the attachment or from the attachment table.</span></span> <span data-ttu-id="dc419-117">この **PR_ATTACH_RENDERING、** 時間がかかりますが、最初の戦略の方が安全です。</span><span class="sxs-lookup"><span data-stu-id="dc419-117">For **PR_ATTACH_RENDERING**, the first strategy, although more time-consuming, is safer.</span></span> <span data-ttu-id="dc419-118">一部のメッセージ ストア プロバイダーはテーブル列を 255 バイトに切り捨てるか、場合によっては 510 バイトに切り捨てるので **、PR_ATTACH_RENDERING** 列に完全なレンダリングが含まれているのを確認することは困難です。</span><span class="sxs-lookup"><span data-stu-id="dc419-118">Because some message store providers truncate their table columns to 255 bytes, or in a few cases 510 bytes, it is difficult to be sure that the **PR_ATTACH_RENDERING** column contains the complete rendering.</span></span> <span data-ttu-id="dc419-119">添付ファイルから直接プロパティを取得すると、常に完了します。</span><span class="sxs-lookup"><span data-stu-id="dc419-119">When retrieving the property directly from the attachment, it will always be complete.</span></span> 
  
<span data-ttu-id="dc419-120">OLE 添付ファイルもメッセージ添付 **ファイルも設定** PR_ATTACH_RENDERING。</span><span class="sxs-lookup"><span data-stu-id="dc419-120">Neither OLE nor message attachments set **PR_ATTACH_RENDERING**.</span></span> <span data-ttu-id="dc419-121">代わりに、OLE 1 添付ファイルのレンダリング情報がメッセージ テキスト ストリームに格納されます。</span><span class="sxs-lookup"><span data-stu-id="dc419-121">Instead, rendering information for OLE 1 attachments is stored in the message text stream.</span></span> <span data-ttu-id="dc419-122">OLE 2 添付ファイルの場合は、ストレージ オブジェクトの特別な子ストリームに格納されます。</span><span class="sxs-lookup"><span data-stu-id="dc419-122">For OLE 2 attachments, it is stored in a special child stream of the storage object.</span></span> <span data-ttu-id="dc419-123">メッセージ添付ファイルのレンダリング情報は、フォーム マネージャーから利用できます。</span><span class="sxs-lookup"><span data-stu-id="dc419-123">Rendering information for message attachments is available through the form manager.</span></span> 
  
 <span data-ttu-id="dc419-124">**メッセージ添付ファイルのレンダリングを取得するには**</span><span class="sxs-lookup"><span data-stu-id="dc419-124">**To retrieve the rendering for a message attachment**</span></span>
  
1. <span data-ttu-id="dc419-125">メッセージのメッセージ クラスを使用して、フォーム マネージャーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="dc419-125">Use the message class of the message to access the form manager.</span></span>
    
2. <span data-ttu-id="dc419-126">フォーム マネージャーのプロパティに **PR_MINI_ICON** します。</span><span class="sxs-lookup"><span data-stu-id="dc419-126">Access the form manager's **PR_MINI_ICON** property.</span></span> <span data-ttu-id="dc419-127">詳細については、「PR_MINI_ICON **(** [PidTagMiniIcon )」を参照してください](pidtagminiicon-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="dc419-127">For more information, see **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span></span>
    

