---
title: 書式設定されたテキストへのレンダリング情報の追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a67fc7cbb3be5c7a23cb85e60dc33d853614cda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420613"
---
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="b78c9-103">書式設定されたテキストへのレンダリング情報の追加</span><span class="sxs-lookup"><span data-stu-id="b78c9-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="b78c9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b78c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b78c9-105">添付ファイルがレンダリングされる書式設定されたテキスト内の場所を指定するには、メッセージの PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティに一 **連の** プレースホルダー文字を挿入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b78c9-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="b78c9-106">プレースホルダー シーケンスは、次の文字で構成されます  `\objattph` 。</span><span class="sxs-lookup"><span data-stu-id="b78c9-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="b78c9-107">**書式設定されたメッセージ テキストにレンダリング情報を追加するには**</span><span class="sxs-lookup"><span data-stu-id="b78c9-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="b78c9-108">テキストのストリームをメッセージの **PR_RTF_COMPRESSED** プロパティに書き込む場合は、プレースホルダー シーケンスとスペース文字を添付ファイルをレンダリングする位置に挿入します。</span><span class="sxs-lookup"><span data-stu-id="b78c9-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="b78c9-109">各添付 **PR_RENDERING_POSITION** の [プロパティ (PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)プロパティを数値に設定します。</span><span class="sxs-lookup"><span data-stu-id="b78c9-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="b78c9-110">書式設定されたテキストに表示する最初PR_RENDERING_POSITION **のプロパティ** に、最も低い値を割り当てる必要があります。最後の添付ファイルの最高値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b78c9-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

