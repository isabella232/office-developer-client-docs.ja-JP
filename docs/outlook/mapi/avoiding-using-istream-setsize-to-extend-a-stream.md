---
title: IStreamSetSize を使用してストリームを拡張しないようにする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428915"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="a6581-103">IStream::SetSize を使用したストリームの拡張の回避</span><span class="sxs-lookup"><span data-stu-id="a6581-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="a6581-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6581-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6581-105">ストリームに書き込む場合、初期サイズが十分ではなくなったため、ストリームを拡大する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6581-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="a6581-106">OLE メソッド **IStream::Write** を使用して **、IStream::SetSize ではなく、これを実行します**。</span><span class="sxs-lookup"><span data-stu-id="a6581-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="a6581-107">**IStream::Write** によってストリームが自動的に拡張され、\*\* IStream::SetSize \*\* が不要になります。</span><span class="sxs-lookup"><span data-stu-id="a6581-107">**IStream::Write** automatically extends the stream, making \*\* IStream::SetSize \*\* unnecessary.</span></span> <span data-ttu-id="a6581-108">**IStream::Write** を **IStream::SetSize** なしで呼び出す場合、書き込み前に **SetSize** 呼び出しを行うよりも最大 3 倍速 **くなります**。</span><span class="sxs-lookup"><span data-stu-id="a6581-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

