---
title: MAPI フォーム
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 951a1c88d2fd4291ee0b48924de6eda8f43c3e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409973"
---
# <a name="mapi-forms"></a><span data-ttu-id="b3155-103">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="b3155-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="b3155-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3155-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3155-105">MAPI フォーム アーキテクチャのこの概要を読んだ後、MAPI フォームの概要と、MAPI サブシステムの他のコンポーネントとの対話方法について理解できます。</span><span class="sxs-lookup"><span data-stu-id="b3155-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="b3155-106">このセクションの目的は、独自の MAPI フォーム サーバーを実装するために必要な概念的な知識を提供します。</span><span class="sxs-lookup"><span data-stu-id="b3155-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="b3155-107">このセクションを読む前に、MAPI フォームの概要トピックの資料 [について理解する必要](mapi-forms-overview.md) があります。</span><span class="sxs-lookup"><span data-stu-id="b3155-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b3155-108">MAPI フォーム アーキテクチャはコンポーネント オブジェクト モデル (COM) に基づくため、フォーム サーバー アプリケーションを開発するには、COM プログラミングに関する知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="b3155-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="b3155-109">COM の詳細については、SDK の「COM と ActiveX オブジェクト サービス」セクションWindowsしてください。</span><span class="sxs-lookup"><span data-stu-id="b3155-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

