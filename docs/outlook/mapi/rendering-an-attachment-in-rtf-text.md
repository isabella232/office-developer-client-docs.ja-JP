---
title: RTF テキストで添付ファイルをレンダリングする
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
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="c090e-103">RTF テキストで添付ファイルをレンダリングする</span><span class="sxs-lookup"><span data-stu-id="c090e-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="c090e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c090e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c090e-105">リッチ テキスト形式 (RTF) 対応のクライアントは、メッセージの **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティで次のエスケープ シーケンスを探して、RTF メッセージ テキストからレンダリングの位置情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="c090e-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="c090e-106">**書式設定されたテキストでレンダリング情報を見つけるには**</span><span class="sxs-lookup"><span data-stu-id="c090e-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="c090e-107">**メッセージの添付ファイル テーブルにアクセスするには、IMessage::GetAttachmentTable** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c090e-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="c090e-108">詳細については [、「IMessage::GetAttachmentTable」を参照してください](imessage-getattachmenttable.md)。</span><span class="sxs-lookup"><span data-stu-id="c090e-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="c090e-109">テーブルを -1 に等しくない行に制限 **PR_RENDERING_POSITIONプロパティ** 制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="c090e-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="c090e-110">詳細については、「PR_RENDERING_POSITION **(** [PidTagRenderingPosition )」を参照してください](pidtagrenderingposition-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="c090e-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="c090e-111">**IMAPITable::Restrict を呼び出して** 制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="c090e-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="c090e-112">詳細については [、「IMAPITable::Restrict」を参照してください](imapitable-restrict.md)。</span><span class="sxs-lookup"><span data-stu-id="c090e-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="c090e-113">**IMAPITable::SortTable を呼び出して** 添付ファイルを並べ替える。</span><span class="sxs-lookup"><span data-stu-id="c090e-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="c090e-114">詳細については [、「IMAPITable::SortTable」を参照してください](imapitable-sorttable.md)。</span><span class="sxs-lookup"><span data-stu-id="c090e-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="c090e-115">**IMAPITable::QueryRows を呼び出して、適切** な行を取得します。</span><span class="sxs-lookup"><span data-stu-id="c090e-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="c090e-116">詳細については [、「IMAPITable::QueryRows」を参照してください](imapitable-queryrows.md)。</span><span class="sxs-lookup"><span data-stu-id="c090e-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="c090e-117">メッセージの **IMAPIProp::OpenProperty** メソッドを呼び出して **、IStream** **インターフェイス** PR_RTF_COMPRESSEDを取得します。</span><span class="sxs-lookup"><span data-stu-id="c090e-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="c090e-118">詳細については [、「IMAPIProp::OpenProperty」および「PR_RTF_COMPRESSED」](imapiprop-openproperty.md) を **参照してください**。</span><span class="sxs-lookup"><span data-stu-id="c090e-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="c090e-119">ストリームをスキャンし、レンダリング プレースホルダーを探します  `\objattph` 。</span><span class="sxs-lookup"><span data-stu-id="c090e-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="c090e-120">このプレースホルダーに続く文字は、並べ替えたテーブル内の次の添付ファイルの場所です。</span><span class="sxs-lookup"><span data-stu-id="c090e-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

