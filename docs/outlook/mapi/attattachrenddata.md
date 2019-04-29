---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427137"
---
# <a name="attattachrenddata"></a><span data-ttu-id="e2aba-103">attAttachRenddata</span><span class="sxs-lookup"><span data-stu-id="e2aba-103">attAttachRenddata</span></span>

  
  
<span data-ttu-id="e2aba-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2aba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2aba-105">**attAttachRenddata**属性は、添付ファイルがメッセージテキスト内でどのようにレンダリングされるかを示す、 **RENDDATA**構造体としてエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="e2aba-105">The **attAttachRenddata** attribute is encoded as a **RENDDATA** structure that describes how and where the attachment is rendered in the message text.</span></span> <span data-ttu-id="e2aba-106">**RENDDATA**構造体は、単に TNEF ストリームで、 **RENDDATA**構造の最初のメンバーから始まる**sizeof (RENDDATA)** バイトでエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="e2aba-106">The **RENDDATA** structure is simply encoded in the TNEF stream as **sizeof(RENDDATA)** bytes beginning with the first member of the **RENDDATA** structure.</span></span> <span data-ttu-id="e2aba-107">**RENDDATA**構造体の**dwFlags**メンバーの値が**MAC_BINARY**に設定されている場合、次の添付ファイルのデータは MacBinary 形式で格納されます。それ以外の場合、添付ファイルデータは通常どおりにエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="e2aba-107">If the value of the **RENDDATA** structure's **dwFlags** member is set to **MAC_BINARY**, then the data for the following attachment is stored in MacBinary format; otherwise, the attachment data is encoded as usual.</span></span>
  

