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
ms.openlocfilehash: e3f35126f3887bc1f2979721deb90891b97c9322
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801375"
---
# <a name="mapi-forms"></a><span data-ttu-id="a6ac4-103">MAPI フォーム</span><span class="sxs-lookup"><span data-stu-id="a6ac4-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="a6ac4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6ac4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6ac4-105">MAPI フォームのアーキテクチャの概要を読むと後は、MAPI フォームとは、MAPI サブシステムの他のコンポーネントとやり取りする方法を理解するがあります。</span><span class="sxs-lookup"><span data-stu-id="a6ac4-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="a6ac4-106">このセクションの目的では、独自の MAPI フォームのサーバーを実装する必要があります概念的な知識を提供します。</span><span class="sxs-lookup"><span data-stu-id="a6ac4-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="a6ac4-107">このセクションを読む前にする必要があります理解する[MAPI フォームの概要](mapi-forms-overview.md)のトピックの内容。</span><span class="sxs-lookup"><span data-stu-id="a6ac4-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a6ac4-108">MAPI フォームのアーキテクチャはコンポーネント オブジェクト モデル (COM) に基づいているためフォームのサーバー アプリケーションを開発すると、COM プログラミングの知識が必要です。</span><span class="sxs-lookup"><span data-stu-id="a6ac4-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="a6ac4-109">COM の詳細については、Windows SDK で、COM および ActiveX オブジェクト サービスのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6ac4-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

