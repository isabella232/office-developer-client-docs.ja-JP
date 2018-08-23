---
title: MAPI アーキテクチャの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a0f2efc17ca8790502f11d677498013cbe10205d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579355"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="50ee5-103">MAPI アーキテクチャの概要</span><span class="sxs-lookup"><span data-stu-id="50ee5-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="50ee5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50ee5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50ee5-105">MAPI は、次の図に示すように、モジュラー型アーキテクチャを定義します。</span><span class="sxs-lookup"><span data-stu-id="50ee5-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="50ee5-106">![Outlook 2010 のアーキテクチャ](media/amapi_43.gif "Outlook 2010 のアーキテクチャ")</span><span class="sxs-lookup"><span data-stu-id="50ee5-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="50ee5-107">MAPI アプリケーションは、MAPI サブシステムのクライアントであるために、クライアント アプリケーションと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="50ee5-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="50ee5-108">メッセージング ベース アプリケーションでは、中心的な処理の一部としてメッセージを使用してし、を保存し、ローカルに情報を整理するのにはさまざまな形式と機能のさまざまな種類の情報の交換など、広範なメッセージング機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="50ee5-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="50ee5-109">E メール、スケジュール、および作業の流れのアプリケーションがメッセージ ベースのアプリケーションの例を示します。</span><span class="sxs-lookup"><span data-stu-id="50ee5-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="50ee5-110">MAPI サブシステムは、共通のユーザー インターフェイスとプログラミング インターフェイスで構成されています。</span><span class="sxs-lookup"><span data-stu-id="50ee5-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="50ee5-111">共通のユーザー インターフェイスは、一貫した外観とユーザーのクライアント アプリケーションを提供する一連のダイアログ ボックスが機能する方法を統一します。</span><span class="sxs-lookup"><span data-stu-id="50ee5-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="50ee5-112">MAPI は MAPI のサブシステム、クライアント ソフトウェアの開発者、およびサービス プロバイダーの開発者によって使用されるインターフェイスのプログラミングを持っています。</span><span class="sxs-lookup"><span data-stu-id="50ee5-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="50ee5-113">MAPI プログラミング ・ インタ フェースは、メイン オブジェクトに基づいたプログラミング インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="50ee5-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="50ee5-114">MAPI プログラミング インターフェイスは、OLE コンポーネント オブジェクト モデルのようなメッセージ ベースのクライアント アプリケーションが C または C++ で記述された、MAPI サブシステムが使用します。</span><span class="sxs-lookup"><span data-stu-id="50ee5-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="50ee5-115">クライアント ソフトウェア開発者は、MAPI プログラミング ・ インタ フェースを使用して直接 MAPI 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="50ee5-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="50ee5-116">1 つの MAPI クライアント インターフェイスまたはインターフェイスの組み合わせとのメッセージングを実装できます。</span><span class="sxs-lookup"><span data-stu-id="50ee5-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="50ee5-117">1 つのアプリケーションは、メソッドまたはインターフェイスのいずれかに属している関数への呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="50ee5-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="50ee5-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="50ee5-118">See also</span></span>

<span data-ttu-id="50ee5-119">-[MAPI の機能とアーキテクチャ](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="50ee5-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

