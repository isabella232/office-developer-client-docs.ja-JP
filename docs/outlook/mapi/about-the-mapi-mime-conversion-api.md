---
title: MAPI-MIME 会話 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575267"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="9b659-103">MAPI-MIME 会話 API について</span><span class="sxs-lookup"><span data-stu-id="9b659-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="9b659-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b659-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b659-105">MAPI から MIME 変換 API では、MAPI メッセージの MIME のオブジェクトとの間で変換するメール プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b659-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="9b659-106">定数の定義、クラス識別子、および[MAPI の定数](mapi-constants.md)のように、インターフェイス識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="9b659-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="9b659-107">メール プロバイダーでは、 **CoCreateInstance**関数を呼び出すことによって、 **[IConverterSession](iconvertersessioniunknown.md)** のインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b659-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

