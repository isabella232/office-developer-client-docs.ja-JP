---
title: MAPI の機能とアーキテクチャ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 75af9598daf4e0d940217504b00cab6d2201d93a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801348"
---
# <a name="mapi-features-and-architecture"></a><span data-ttu-id="b5c9d-103">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="b5c9d-103">MAPI Features and Architecture</span></span>

  
  
<span data-ttu-id="b5c9d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5c9d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5c9d-105">メッセージ API (MAPI) は、共通のアプリケーション プログラミング インターフェイスのセットと、ダイナミック リンク ライブラリ (DLL) のコンポーネントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b5c9d-105">Messaging API (MAPI) is composed of a set of common application programming interfaces and a dynamic-link library (DLL) component.</span></span> <span data-ttu-id="b5c9d-106">作成し、さまざまなメッセージング アプリケーションとメッセージング システムの開発と使用、統一された環境を提供する、両方の真の独立性を提供することをアクセスのインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="b5c9d-106">The interfaces are used to create and access diverse messaging applications and messaging systems, offering a uniform environment for development and use, and providing true independence for both.</span></span> <span data-ttu-id="b5c9d-107">DLL には、メッセージング アプリケーションのフロント エンドおよびバック エンドのメッセージング システム間の相互作用を管理し、頻繁に行う作業の共通のユーザー インターフェイスを提供する MAPI のサブシステムが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5c9d-107">The DLL contains the MAPI subsystem, which manages the interaction between front-end messaging applications and back-end messaging systems and provides a common user interface for frequent tasks.</span></span> <span data-ttu-id="b5c9d-108">MAPI サブシステムは、さまざまなメッセージング システムを統一し、それらの相違点からクライアントを保護する中央のクリアリング ハウスとして機能します。</span><span class="sxs-lookup"><span data-stu-id="b5c9d-108">The MAPI subsystem acts as a central clearinghouse to unify the various messaging systems and shield clients from their differences.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b5c9d-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5c9d-109">See also</span></span>



[<span data-ttu-id="b5c9d-110">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="b5c9d-110">MAPI Concepts</span></span>](mapi-concepts.md)

