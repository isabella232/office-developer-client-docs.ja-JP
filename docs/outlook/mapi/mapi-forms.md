---
title: MAPI フォーム
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b53cdb4fe379405018555f1cca9fa40ddc5d0fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592487"
---
# <a name="mapi-forms"></a><span data-ttu-id="77e3c-103">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="77e3c-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="77e3c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77e3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77e3c-105">MAPI フォームのアーキテクチャの概要を読むと後は、MAPI フォームとは、MAPI サブシステムの他のコンポーネントとやり取りする方法を理解するがあります。</span><span class="sxs-lookup"><span data-stu-id="77e3c-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="77e3c-106">このセクションの目的では、独自の MAPI フォームのサーバーを実装する必要があります概念的な知識を提供します。</span><span class="sxs-lookup"><span data-stu-id="77e3c-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="77e3c-107">このセクションを読む前にする必要があります理解する[MAPI フォームの概要](mapi-forms-overview.md)のトピックの内容。</span><span class="sxs-lookup"><span data-stu-id="77e3c-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="77e3c-108">MAPI フォームのアーキテクチャはコンポーネント オブジェクト モデル (COM) に基づいているためフォームのサーバー アプリケーションを開発すると、COM プログラミングの知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="77e3c-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="77e3c-109">COM の詳細については、Windows SDK で、COM および ActiveX オブジェクト サービスのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77e3c-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

