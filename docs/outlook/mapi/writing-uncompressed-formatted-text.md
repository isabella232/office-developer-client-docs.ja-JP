---
title: 非圧縮書式付きテキストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d34168743926681ee7169a593e302755b193aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577045"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="4871c-103">非圧縮書式付きテキストの作成</span><span class="sxs-lookup"><span data-stu-id="4871c-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="4871c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4871c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4871c-105">書式設定されたテキストを含むメッセージを送信する準備ができたら、いずれかの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティをメッセージの圧縮または非圧縮のテキストに設定します。</span><span class="sxs-lookup"><span data-stu-id="4871c-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="4871c-106">**PR_RTF_COMPRESSED**プロパティに圧縮されたテキストを書き込む、非常に CPU 負荷の高い操作は、パフォーマンスに大きく影響します。</span><span class="sxs-lookup"><span data-stu-id="4871c-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="4871c-107">、書式設定されたメッセージを送信するか、パフォーマンスを向上します。</span><span class="sxs-lookup"><span data-stu-id="4871c-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="4871c-108">CPU は常に可能なソリューションをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="4871c-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="4871c-109">または、</span><span class="sxs-lookup"><span data-stu-id="4871c-109">Or -</span></span>
    
- <span data-ttu-id="4871c-110">**PR_RTF_COMPRESSED**プロパティには、圧縮されていないテキストを作成します。</span><span class="sxs-lookup"><span data-stu-id="4871c-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="4871c-111">**PR_RTF_COMPRESSED**に圧縮されていないテキストを設定する手順は、例外が 1 つの圧縮されたテキストを設定することと同じです。</span><span class="sxs-lookup"><span data-stu-id="4871c-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="4871c-112">[WrapCompressedRTFStream](wrapcompressedrtfstream.md)を呼び出すときは、 _ulFlags_パラメーターで STORE_UNCOMPRESSED_RTF フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="4871c-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="4871c-113">メッセージのサイズが増加するという点で欠点には圧縮されていないテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="4871c-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

