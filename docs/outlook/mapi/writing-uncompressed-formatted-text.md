---
title: 圧縮されていない書式付きテキストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325754"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="23e7e-103">圧縮されていない書式付きテキストの作成</span><span class="sxs-lookup"><span data-stu-id="23e7e-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="23e7e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23e7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23e7e-105">書式設定されたテキストを使用してメッセージを送信する準備をするときは、メッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを圧縮または圧縮しないテキストに設定します。</span><span class="sxs-lookup"><span data-stu-id="23e7e-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="23e7e-106">**PR_RTF_COMPRESSED**プロパティに圧縮されたテキストを書き込むことは、CPU を集中的に使用する操作であり、パフォーマンスに大きく影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="23e7e-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="23e7e-107">書式設定されたメッセージの送信のパフォーマンスを向上させるには、次のいずれかを行います。</span><span class="sxs-lookup"><span data-stu-id="23e7e-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="23e7e-108">CPU をアップグレードします。これは、常に問題を解決するものではありません。</span><span class="sxs-lookup"><span data-stu-id="23e7e-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="23e7e-109">や</span><span class="sxs-lookup"><span data-stu-id="23e7e-109">Or -</span></span>
    
- <span data-ttu-id="23e7e-110">**PR_RTF_COMPRESSED**プロパティに圧縮されていないテキストを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="23e7e-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="23e7e-111">圧縮されていないテキストを使用して**PR_RTF_COMPRESSED**を設定する手順は、1つの例外を除き、圧縮テキストを設定する手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="23e7e-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="23e7e-112">[WrapCompressedRTFStream](wrapcompressedrtfstream.md)を呼び出すときは、 _ulflags_パラメーターに STORE_UNCOMPRESSED_RTF フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="23e7e-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="23e7e-113">圧縮されていないテキストを設定すると、メッセージのサイズが大きくなるという欠点があります。</span><span class="sxs-lookup"><span data-stu-id="23e7e-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

