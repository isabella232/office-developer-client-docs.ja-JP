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
# <a name="mapi-features-and-architecture"></a><span data-ttu-id="cf8d6-103">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="cf8d6-103">MAPI Features and Architecture</span></span>

  
  
<span data-ttu-id="cf8d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf8d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf8d6-105">メッセージング API (MAPI) は、一般的なアプリケーション プログラミング インターフェイスのセットと、ダイナミック リンク ライブラリ (DLL) コンポーネントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="cf8d6-105">Messaging API (MAPI) is composed of a set of common application programming interfaces and a dynamic-link library (DLL) component.</span></span> <span data-ttu-id="cf8d6-106">インターフェイスは、多様なメッセージング アプリケーションとメッセージング システムの作成とアクセスに使用され、開発と使用のための均一な環境を提供し、両方に真の独立性を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf8d6-106">The interfaces are used to create and access diverse messaging applications and messaging systems, offering a uniform environment for development and use, and providing true independence for both.</span></span> <span data-ttu-id="cf8d6-107">DLL には MAPI サブシステムが含まれています。このサブシステムは、フロントエンド メッセージング アプリケーションとバック エンド メッセージング システム間のやり取りを管理し、頻繁なタスクに共通のユーザー インターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="cf8d6-107">The DLL contains the MAPI subsystem, which manages the interaction between front-end messaging applications and back-end messaging systems and provides a common user interface for frequent tasks.</span></span> <span data-ttu-id="cf8d6-108">MAPI サブシステムは、さまざまなメッセージング システムを統合し、クライアントの違いを保護する中央クリアリングハウスとして機能します。</span><span class="sxs-lookup"><span data-stu-id="cf8d6-108">The MAPI subsystem acts as a central clearinghouse to unify the various messaging systems and shield clients from their differences.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf8d6-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf8d6-109">See also</span></span>



[<span data-ttu-id="cf8d6-110">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="cf8d6-110">MAPI Concepts</span></span>](mapi-concepts.md)

