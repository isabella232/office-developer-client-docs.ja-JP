---
title: IStreamSetSize を使用してストリームを拡張することを避ける
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799749"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="fb755-103">IStream::SetSize を使用してストリームを拡張することを避ける</span><span class="sxs-lookup"><span data-stu-id="fb755-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="fb755-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb755-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb755-105">、ストリームに書き込むときの初期サイズが十分でないために、それらを拡大する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb755-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="fb755-106">OLE メソッド**IStream::Write**を使用して、これを実現する**IStream::SetSize**ではなく。</span><span class="sxs-lookup"><span data-stu-id="fb755-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="fb755-107">**IStream::Write**は、ストリームを自動的に拡張すること * * IStream::SetSize * * 不要な。</span><span class="sxs-lookup"><span data-stu-id="fb755-107">**IStream::Write** automatically extends the stream, making ** IStream::SetSize ** unnecessary.</span></span> <span data-ttu-id="fb755-108">**IStream::SetSize**に**IStream::Write**を呼び出すことは、3 回まで呼び出し**を記述**する前に、 **SetSize**を行うよりも高速。</span><span class="sxs-lookup"><span data-stu-id="fb755-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

