---
title: MAPI-MIME 会話 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321820"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="b8a6e-103">MAPI-MIME 会話 API について</span><span class="sxs-lookup"><span data-stu-id="b8a6e-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="b8a6e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8a6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8a6e-105">mapi-mime 変換 API を使用すると、メールプロバイダーは MIME オブジェクトと MAPI メッセージ間で変換することができます。</span><span class="sxs-lookup"><span data-stu-id="b8a6e-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="b8a6e-106">このメソッドは、 [MAPI 定数](mapi-constants.md)に示されているように、定数定義、クラス識別子、およびインターフェイス識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="b8a6e-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="b8a6e-107">メールプロバイダーは、 **CoCreateInstance**関数を呼び出すことによって、 **[iconvertersession](iconvertersessioniunknown.md)** のインスタンスを cocreate する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8a6e-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

