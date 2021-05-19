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
# <a name="mapi-architecture-overview"></a><span data-ttu-id="a2061-103">MAPI アーキテクチャの概要</span><span class="sxs-lookup"><span data-stu-id="a2061-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="a2061-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2061-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2061-105">MAPI は、次の図に示すように、モジュール型アーキテクチャを定義します。</span><span class="sxs-lookup"><span data-stu-id="a2061-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="a2061-106">![Outlook 2010 アーキテクチャ](media/amapi_43.gif "Outlook 2010 アーキテクチャ")</span><span class="sxs-lookup"><span data-stu-id="a2061-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="a2061-107">MAPI アプリケーションは、MAPI サブシステムのクライアントなので、クライアント アプリケーションと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="a2061-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="a2061-108">メッセージング ベースのアプリケーションは、メッセージングを処理の中心的な部分として採用し、さまざまな種類の情報をさまざまな形式で交換し、情報をローカルに保存および整理する機能など、広範なメッセージング機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2061-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="a2061-109">メール、スケジュール、および作業フロー アプリケーションは、メッセージング ベースのアプリケーションの例です。</span><span class="sxs-lookup"><span data-stu-id="a2061-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="a2061-110">MAPI サブシステムは、一般的なユーザー インターフェイスとプログラミング インターフェイスで構成されます。</span><span class="sxs-lookup"><span data-stu-id="a2061-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="a2061-111">一般的なユーザー インターフェイスは、クライアント アプリケーションに一貫性のある外観を提供し、ユーザーが一貫した動作方法を提供する一連のダイアログ ボックスです。</span><span class="sxs-lookup"><span data-stu-id="a2061-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="a2061-112">MAPI には、MAPI サブシステム、クライアント ソフトウェア開発者、およびサービス プロバイダー開発者が使用するプログラミング インターフェイスがあります。</span><span class="sxs-lookup"><span data-stu-id="a2061-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="a2061-113">MAPI プログラミング インターフェイスは、主なオブジェクト ベースのプログラミング インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="a2061-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="a2061-114">MAPI プログラミング インターフェイスは OLE コンポーネント オブジェクト モデルに似ていて、MAPI サブシステムと、C または C++ で記述されたメッセージング ベースのクライアント アプリケーションで使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2061-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="a2061-115">クライアント ソフトウェア開発者は、MAPI プログラミング インターフェイスを介して MAPI 呼び出しを直接行います。</span><span class="sxs-lookup"><span data-stu-id="a2061-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="a2061-116">1 つの MAPI クライアント インターフェイスまたはインターフェイスの組み合わせでメッセージングを実装できます。</span><span class="sxs-lookup"><span data-stu-id="a2061-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="a2061-117">1 つのアプリケーションで、任意のインターフェイスに属するメソッドまたは関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a2061-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2061-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2061-118">See also</span></span>

<span data-ttu-id="a2061-119">-[MAPI の機能とアーキテクチャ](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="a2061-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

