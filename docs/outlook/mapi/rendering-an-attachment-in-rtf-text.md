---
title: RTF テキスト形式での添付ファイルのレンダリング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439794"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="01ac1-103">RTF テキスト形式での添付ファイルのレンダリング</span><span class="sxs-lookup"><span data-stu-id="01ac1-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="01ac1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01ac1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01ac1-105">リッチテキスト形式 (rtf) 対応クライアントは、メッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティで次のエスケープシーケンスを検索することによって、rtf メッセージテキストからレンダリング位置情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="01ac1-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="01ac1-106">**書式設定されたテキストでレンダリング情報を検索するには**</span><span class="sxs-lookup"><span data-stu-id="01ac1-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="01ac1-107">メッセージの添付ファイルテーブルにアクセスするには、 **IMessage:: getattachmenttable**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01ac1-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="01ac1-108">詳細については、「 [IMessage:: getattachmenttable](imessage-getattachmenttable.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01ac1-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="01ac1-109">**PR_RENDERING_POSITION**が-1 と等しくない行にテーブルを制限するプロパティ制限を構築します。</span><span class="sxs-lookup"><span data-stu-id="01ac1-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="01ac1-110">詳細については、「 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01ac1-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="01ac1-111">**IMAPITable:: Restrict**を呼び出して制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="01ac1-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="01ac1-112">詳細については、「 [IMAPITable:: Restrict](imapitable-restrict.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01ac1-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="01ac1-113">呼び出し**IMAPITable:: sorttable**は、添付ファイルを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="01ac1-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="01ac1-114">詳細については、「 [IMAPITable:: sorttable](imapitable-sorttable.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01ac1-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="01ac1-115">必要な行を取得するには、 **IMAPITable:: QueryRows**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01ac1-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="01ac1-116">詳細については、「 [IMAPITable:: QueryRows](imapitable-queryrows.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01ac1-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="01ac1-117">メッセージの**imapiprop:: openproperty**メソッドを呼び出して、 **IStream**インターフェイスを使用して**PR_RTF_COMPRESSED**を取得します。</span><span class="sxs-lookup"><span data-stu-id="01ac1-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="01ac1-118">詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01ac1-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="01ac1-119">ストリームをスキャンして、レンダリングプレースホルダーを探し`\objattph`ます。</span><span class="sxs-lookup"><span data-stu-id="01ac1-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="01ac1-120">このプレースホルダーの後の文字は、並べ替えられたテーブルの次の添付ファイルの場所です。</span><span class="sxs-lookup"><span data-stu-id="01ac1-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

