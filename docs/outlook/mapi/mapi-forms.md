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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351346"
---
# <a name="mapi-forms"></a><span data-ttu-id="4c32e-103">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="4c32e-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="4c32e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c32e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c32e-105">mapi フォームアーキテクチャの概要を読み終えたら、mapi フォームの内容と mapi サブシステムの他のコンポーネントとの対話方法について理解します。</span><span class="sxs-lookup"><span data-stu-id="4c32e-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="4c32e-106">このセクションの目的は、独自の MAPI フォームサーバーを実装するために必要な概念知識を得ることです。</span><span class="sxs-lookup"><span data-stu-id="4c32e-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="4c32e-107">このセクションを読む前に、「 [MAPI フォームの概要](mapi-forms-overview.md)」のトピックの内容を理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c32e-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4c32e-108">MAPI フォームのアーキテクチャはコンポーネントオブジェクトモデル (com) に基づいているため、フォームサーバーアプリケーションを開発するには、com プログラミングに関する知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="4c32e-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="4c32e-109">com の詳細については、Windows SDK の「com および ActiveX のオブジェクトサービス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c32e-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

