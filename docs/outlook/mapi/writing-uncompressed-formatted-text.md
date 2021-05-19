---
title: 圧縮されていない書式設定されたテキストの書き込み
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426325"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="aaf9f-103">圧縮されていない書式設定されたテキストの書き込み</span><span class="sxs-lookup"><span data-stu-id="aaf9f-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="aaf9f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf9f-105">書式設定されたテキストを含むメッセージを送信する準備をする場合は、メッセージの **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを圧縮テキストまたは非圧縮テキストに設定します。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="aaf9f-106">PR_RTF_COMPRESSED プロパティに圧縮されたテキスト **を書き込** むのは、CPU の負荷が非常に高い操作であり、パフォーマンスに大きな影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="aaf9f-107">書式設定されたメッセージの送信のパフォーマンスを向上するには、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="aaf9f-108">必ずしももっともらしいとは限りないソリューションである CPU をアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="aaf9f-109">Or -</span><span class="sxs-lookup"><span data-stu-id="aaf9f-109">Or -</span></span>
    
- <span data-ttu-id="aaf9f-110">圧縮されていないテキストを PR_RTF_COMPRESSED プロパティ **に記述** します。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="aaf9f-111">圧縮されていない **テキストPR_RTF_COMPRESSED設定** する手順は、1 つの例外を除き、圧縮されたテキストで設定する手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="aaf9f-112">[WrapCompressedRTFStream](wrapcompressedrtfstream.md)を呼び出す場合は _、ulFlags_ パラメーター STORE_UNCOMPRESSED_RTFフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="aaf9f-113">圧縮されていないテキストを設定すると、メッセージのサイズが大きという欠点があります。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

