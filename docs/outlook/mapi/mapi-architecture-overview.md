---
title: MAPI アーキテクチャの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410078"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="f87f5-103">MAPI アーキテクチャの概要</span><span class="sxs-lookup"><span data-stu-id="f87f5-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="f87f5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f87f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f87f5-105">MAPI では、次の図に示すように、モジュラーアーキテクチャが定義されています。</span><span class="sxs-lookup"><span data-stu-id="f87f5-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="f87f5-106">![Outlook 2010 アーキテクチャ](media/amapi_43.gif "Outlook 2010 アーキテクチャ")</span><span class="sxs-lookup"><span data-stu-id="f87f5-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="f87f5-107">mapi アプリケーションは、mapi サブシステムのクライアントであるため、クライアントアプリケーションと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f87f5-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="f87f5-108">メッセージングベースのアプリケーションは、メッセージングを処理の中心的な部分として使用し、さまざまな種類の情報をさまざまな形式で交換したり、情報をローカルに保存および整理したりするなど、広範なメッセージング機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="f87f5-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="f87f5-109">メール、スケジュール、およびワークフローのアプリケーションは、メッセージングベースのアプリケーションの例です。</span><span class="sxs-lookup"><span data-stu-id="f87f5-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="f87f5-110">MAPI サブシステムは、共通のユーザーインターフェイスとプログラミングインターフェイスで構成されています。</span><span class="sxs-lookup"><span data-stu-id="f87f5-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="f87f5-111">共通のユーザーインターフェイスは一連のダイアログボックスで、クライアントアプリケーションに一貫した外観とユーザーを提供し、一貫した方法で作業を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f87f5-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="f87f5-112">mapi は、mapi サブシステム、クライアントソフトウェア開発者、およびサービスプロバイダー開発者によって使用されるプログラミングインターフェイスを備えています。</span><span class="sxs-lookup"><span data-stu-id="f87f5-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="f87f5-113">MAPI プログラミングインターフェイスは、主要なオブジェクトベースのプログラミングインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="f87f5-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="f87f5-114">mapi プログラミングインターフェイスは OLE コンポーネントオブジェクトモデルに似ており、C または C++ で記述された mapi サブシステムおよびメッセージングベースのクライアントアプリケーションによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="f87f5-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="f87f5-115">クライアントソフトウェア開発者は、mapi のプログラミングインターフェイスを使用して mapi を直接呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f87f5-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="f87f5-116">単一の MAPI クライアントインターフェイスまたはインターフェイスの組み合わせを使用して、メッセージングを実装できます。</span><span class="sxs-lookup"><span data-stu-id="f87f5-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="f87f5-117">1つのアプリケーションで、いずれかのインターフェイスに属するメソッドまたは関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f87f5-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f87f5-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="f87f5-118">See also</span></span>

<span data-ttu-id="f87f5-119">-[MAPI の機能とアーキテクチャ](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="f87f5-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

