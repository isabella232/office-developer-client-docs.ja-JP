---
title: Rtf 形式のテキストの添付ファイルを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cf22e360a0319a662c9b7dd31856dbb6eccec02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803742"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="822e1-103">Rtf 形式のテキストの添付ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="822e1-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="822e1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="822e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="822e1-105">リッチ テキスト形 (式 RTF) に対応していないクライアントはメッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティで、次のエスケープ シーケンスを探すことで RTF メッセージ テキストのレンダリング位置の情報を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="822e1-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="822e1-106">**書式設定されたテキストのレンダリング情報を検索するには**</span><span class="sxs-lookup"><span data-stu-id="822e1-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="822e1-107">メッセージの添付ファイル テーブルにアクセスするのには**IMessage::GetAttachmentTable**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="822e1-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="822e1-108">詳細については、 [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="822e1-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="822e1-109">**PR_RENDERING_POSITION** -1 と等しくないの行にテーブルを制限するプロパティの制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="822e1-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="822e1-110">詳細については、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="822e1-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="822e1-111">制限を強制するのには**IMAPITable::Restrict**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="822e1-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="822e1-112">詳細については、 [IMAPITable::Restrict](imapitable-restrict.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="822e1-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="822e1-113">添付ファイルを並べ替えるには**IMAPITable::SortTable**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="822e1-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="822e1-114">詳細については、 [IMAPITable::SortTable](imapitable-sorttable.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="822e1-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="822e1-115">適切な行を取得するために**IMAPITable::QueryRows**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="822e1-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="822e1-116">詳細については、 [IMAPITable::QueryRows](imapitable-queryrows.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="822e1-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="822e1-117">**PR_RTF_COMPRESSED**を**IStream**インターフェイスを取得するために、メッセージの**IMAPIProp::OpenProperty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="822e1-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="822e1-118">詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **PR_RTF_COMPRESSED**を参照してください。</span><span class="sxs-lookup"><span data-stu-id="822e1-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="822e1-119">レンダリングのプレース ホルダーを探して、ストリームをスキャンする`\objattph`。</span><span class="sxs-lookup"><span data-stu-id="822e1-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="822e1-120">このプレース ホルダーを次の文字は、並べ替えられたテーブルに次の添付ファイルの場所です。</span><span class="sxs-lookup"><span data-stu-id="822e1-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

