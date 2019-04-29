---
title: MAPI の機能とアーキテクチャ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8156cb53fc81f4861e4a66da4960df0458ec6c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418282"
---
# <a name="mapi-features-and-architecture"></a><span data-ttu-id="4ac91-103">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="4ac91-103">MAPI Features and Architecture</span></span>

  
  
<span data-ttu-id="4ac91-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ac91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ac91-105">メッセージング API (MAPI) は、一般的なアプリケーションプログラミングインターフェイスのセットと、ダイナミックリンクライブラリ (DLL) コンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="4ac91-105">Messaging API (MAPI) is composed of a set of common application programming interfaces and a dynamic-link library (DLL) component.</span></span> <span data-ttu-id="4ac91-106">このインターフェイスは、さまざまなメッセージングアプリケーションおよびメッセージングシステムを作成してアクセスし、開発および使用するための一様な環境を提供し、両方に対して真の独立性を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4ac91-106">The interfaces are used to create and access diverse messaging applications and messaging systems, offering a uniform environment for development and use, and providing true independence for both.</span></span> <span data-ttu-id="4ac91-107">DLL には MAPI サブシステムが含まれており、フロントエンドメッセージングアプリケーションとバックエンドメッセージングシステムの間の相互作用を管理し、頻繁にタスクを行うための共通のユーザーインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="4ac91-107">The DLL contains the MAPI subsystem, which manages the interaction between front-end messaging applications and back-end messaging systems and provides a common user interface for frequent tasks.</span></span> <span data-ttu-id="4ac91-108">MAPI サブシステムは、さまざまなメッセージングシステムを統合し、それらの違いからクライアントをシールドするための中央クリアリングとして機能します。</span><span class="sxs-lookup"><span data-stu-id="4ac91-108">The MAPI subsystem acts as a central clearinghouse to unify the various messaging systems and shield clients from their differences.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ac91-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ac91-109">See also</span></span>



[<span data-ttu-id="4ac91-110">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="4ac91-110">MAPI Concepts</span></span>](mapi-concepts.md)

