---
title: MAPI-MIME 会話 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420438"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="301bb-103">MAPI-MIME 会話 API について</span><span class="sxs-lookup"><span data-stu-id="301bb-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="301bb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="301bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="301bb-105">MAPI-MIME 変換 API を使用すると、メール プロバイダーは MIME オブジェクトと MAPI メッセージの間で変換できます。</span><span class="sxs-lookup"><span data-stu-id="301bb-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="301bb-106">MAPI 定数に示すように、定数定義、クラス識別子、およびインターフェイス [識別子を提供します](mapi-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="301bb-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="301bb-107">メール プロバイダーは **、CoCreateInstance** 関数を呼び出して **[IConverterSession](iconvertersessioniunknown.md)** のインスタンスを共同作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="301bb-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

