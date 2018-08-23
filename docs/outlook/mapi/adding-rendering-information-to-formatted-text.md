---
title: 書式付きテキストへのレンダリング情報の追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a6018c05d1191211242066425e4ae546c1618094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594559"
---
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="c8977-103">書式付きテキストへのレンダリング情報の追加</span><span class="sxs-lookup"><span data-stu-id="c8977-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="c8977-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8977-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8977-105">添付ファイルが表示される書式設定されたテキストの位置を指定するには、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティをメッセージのプレース ホルダー文字のシーケンスを挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8977-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="c8977-106">プレース ホルダーの順序は、次の文字で構成されて: `\objattph`。</span><span class="sxs-lookup"><span data-stu-id="c8977-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="c8977-107">**テキストの書式設定されたメッセージにレンダリング情報を追加するのには**</span><span class="sxs-lookup"><span data-stu-id="c8977-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="c8977-108">**PR_RTF_COMPRESSED**プロパティをメッセージのテキストのストリームを作成する場合は、添付ファイルを表示する位置にプレース ホルダーの順序および空白文字を挿入します。</span><span class="sxs-lookup"><span data-stu-id="c8977-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="c8977-109">数値の各添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c8977-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="c8977-110">書式設定されたテキストで表示するのには、最初の添付ファイルの**PR_RENDERING_POSITION**プロパティに最小値を割り当てる必要があります。最後の添付ファイルの最大値です。</span><span class="sxs-lookup"><span data-stu-id="c8977-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

